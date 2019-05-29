# CGDN-SpringBoot-MultipleModules
## Trong bài này chúng ta chia dự án code thành các module nhỏ. Mỗi module phụ trách một công việc độc lập.
1. File POM.XML ngoài cùng hay còn goi là parent
   + File Parent pom chứa các dependencies chung cho các module con <br>
   + File Parent chứa các modules con của nó <br>
2. Module demo-web
   + Chỉ chứa các dependencies phục vụ cho web <br>
   + Không chức các task vụ cho database hoặc các task vụ khác <br>
3. Module demo-business-service	
   + Chỉ chứa những chức năng phục vụ cho bussiness của app <br>
   + Nếu cần các chức năng thao tác database thì mình nhúng module demo-dao vào và sử dụng các interface để query db <br>
4. Module demo-dao
   + Chỉ chứa những chức năng thao tác với database <br>
   + Nếu module nào cần thì nhúng vào module đó <br>
5. Module demo-webservice
   + Chỉ chứa những chức năng liên quan đến webservice  <br> 
   + Không khai báo và sử dụng query ở đây. Nếu cần thì nhúng module demo-dao vào file pox <br>
6. Module demo-common
   + Khai báo các thư viện chung cho toàn bộ module <br>
7. Module demo-configure
   + Khai báo các môi trường UAT, PRODUCTION  <br>
