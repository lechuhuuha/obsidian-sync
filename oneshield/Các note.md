xem lại thư viện copy có các trường sai so với api hiện tại

intergration test cho infra (cần theo kiểu table, đọc trên mạng)
 
xem lại struct field (sai so với api hiện tại)


- thêm 1 function riêng cho bên pfsense pkg để test connection
func cuối trước khi return cho gob thì return sperrors

còn lại log vào file


struct trong service ko cần json khi ko cần marshall

dùng utils.Map để map DTO

sửa lại hàm replyerror để check nếu error đã wrap sperrors rồi thì trả về luôn
ko thì lấy ra error rồi wrap lại bằng sperrors


rm -rf pfsense-api/
git clone https://github.com/lechuhuuha/pfsense-api.git
cd pfsense-api/

pkg-static delete pfSense-pkg-RESTAPI

pfsense-restapi delete

composer i

python3 tools/make_package.py --branch master --tag v2.0.3

cp -r vendor/* pfSense-pkg-RESTAPI/files/usr/local/pkg/RESTAPI/.resources/includes

rm -rf pfSense-pkg-RESTAPI/files/usr/local/pkg/RESTAPI/.resources/includes/composer && rm pfSense-pkg-RESTAPI/files/usr/local/pkg/RESTAPI/.resources/includes/autoload.php


pkg-static -C /dev/null add /root/pfsense-api/pfSense-pkg-RESTAPI/work/pkg/pfSense-pkg-RESTAPI-2.0_3.pkg

/etc/rc.restart_webgui




