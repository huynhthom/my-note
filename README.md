# Github

## Clone code
	git clone https://github.com/SCIREN/tnmt_softs.git
	cd {folder}
	composer install
	cp .env.example .env
	php artisan key:generate
	nếu có csdl tạo bằng migration -> php artisan migrate
	php artisan config:cache
	php artisan view:clear

## Tạo Branches
	git checkout -b thom_tnmt_softs
	git init
	git add -A
	git commit -m "thom_tnmt_sofs"
	git push origin thom_tnmt_softs
	git stash => Lưu bộ nhớ tạm khi đang việc mà muốn checkout vào branch mới
	git stash apply => Apply toàn bộ code đang làm vào luôn
	git branch -m `tên mới` => Đổi tên branch
## Project mới
	git clone địa_chỉ
	git add
	git commit -m "điền nội dung commit vào đây"
	git push origin master

## Pull code from master branch
+ git branch --merged | grep -v \* | xargs git branch -D  => delete branch local
+ git fetch --all
+ git pull origin master
+ Nếu config thì git stash sau đó pull lại
+ git checkout -b `new branch`
## Đổi ổ lưu trữ dữ liệu của WebApp

-  Đối đường dẫn chứa folder web htdocs: `C:\xampp\apache\conf\httpd.conf`
   - Dòng 252, 253
	DocumentRoot `"D:/GIS and RS/WebApps_localhost_xampp"`

			Directory "D:/GIS and RS/WebApps_localhost_xampp"

- Đổi đường dẫn chứa folder webapps tomcat: Copy webapp đến ổ đĩa mình muốn -> đổi tên Dòng 152, 153 `C:\xampp\tomcat\conf\server.xml`
	
			Host name="localhost"  appBase="D:/GIS and RS/Tomcat workspaces" unpackWARs="true" autoDeploy="true"

- Đối đường dẫn chứa data của postgreSQL: 
	`https://wiki.postgresql.org/wiki/Change_the_default_PGDATA_directory_on_Windows`

# Open folder code bằng cmd
- Đối với Notepad++: notepad++ `-openFoldersAsWorkspace {path folder}`
- Đối với VS code: cd {folder} -> `code .`
- Đối với Phpstorm: `phpstorm64.exe {path folder}` (phải đặt biến môi trường trước)

		"C:\Program Files\PostgreSQL\13\bin\pg_ctl.exe" runservice -N "postgresql-x64-13" -D "C:\Program Files\PostgreSQL\13\data" -w
cluster

# Postgresql

## Dùng CMD:
- Backup bảng trống: CMD => `pg_dump -U postgres -W -F t tnmt > D:\Co_quan\moitruong_database\sql\tnmt.sql`
- Backup bảng có dữ liệu: `pg_dump -U postgres -W -F p tnmt > D:\Co_quan\moitruong_database\sql\tnmt.sql`  
-  Restore data: CMD => `psql -U postgres -d tnmt < D:\Co_quan\moitruong_database\sql\tnmt.sql`

## Nếu dùng Terminal: 
-  `psql -U postgres -d YourDatabase -f D:\Backup\.sql `

-  `Create extension postgis`

# Laravel

- Create Larave project: `composer create-project laravel/laravel example-app`
- ClearCode: 
  - `php artisan config:cache`
  - `php artisan view:clear`
- Create Controler:	`php artisan make:controller ProvisionServer`
- Create Modal:	`php artisan make:model Goalscorer`

# Server
```
IP Private User/Password
http://10.151.45.15/ administrator/QWErty@Miennam753159 Product chính
http://10.151.45.9/ administrator/QWErty@Miennam753159
http://10.151.45.3/ administrator/QWErty@Miennam29112021
http://10.151.45.4/ administrator/PortalHCM@1082021

IP Public
210.245.96.141 = 10.151.45.15 Product chính
210.245.96.135 = 10.151.45.9
210.245.96.129 = 10.151.45.3
210.245.96.130 = 10.151.45.4

Linux:
210.245.96.134: 10.151.45.8
sciren_linux/Sciren@123456
```
```
CSDL:
10.151.45.15: postgres 13: postgres/9zfX8#*V8!#tA%hh+dz2?N9?
```

# Link 
- Giống như W3school: `https://developer.mozilla.org/`
- Trực quang Flex: `https://codepen.io/enxaneta/full/adLPwv/`
- Roadmap FE: `https://roadmap.sh/frontend`
- Solidjs: `https://www.solidjs.com/`

# Create project `Tailwindcss` in node
1. >npm init
2. >npm install -g
3. >npm install -y
4. >npm install -D tailwindcss postcss autoprefixer vite
5. >npx tailwindcss init -p
6. >mkdir css
7. create `tailwind.css` file.
8. Add code to `tailwind.css` file.
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
9. >npx tailwindcss-cli build css/tailwind.css -o build/tailwind.css
10. >npm run dev