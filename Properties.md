# Properties class
________________________________________________________________________________
## 1. Giới thiệu
* `Properties` class `extends` từ `Hashtable` class
* `Properties` class được đóng gói trong `java.util.Properties`
* `Properties` class được **sử dụng** để
  * __tạo ra__ đối tượng chứa cặp `key-value` như 1 chuỗi
  * __lấy__ `value`dựa trên `key` của thuộc tính
  * __lấy__ các thuộc tính hay `property` của `System`
* `Properties` class cung cấp các `method` để lấy dữ liệu ra hoặc ghi dữ liệu vào từ các file `.properties`
* Nếu có bất kỳ thay đổi nào từ phía file `.properties`, ta cũng không cần phải compile lại file `.java`
* `Properties` class trong `package` `java.util.Properties` được declare như sau:

```java
public class Properties extends Hashtable<Object, Object> {
    // There are something here...
}
```
________________________________________________________________________________
## 2. Một số quy tắc trong file `.properties`
|Quy tắc|Mẫu|
|-------------|--------|
|Mỗi cặp `key=value` được viết trên 1 dòng, và được phân cách bởi dấu `=`|`key=value`|
|`keyName` không được chứa khoảng trắng, `key Name` là SAI|`keyName`|
|có thể thêm `khoảng trắng` ở 2 đầu của `key` hoặc `value`, mặc định `Properties` class sẽ tự loại bỏ|` key = value ` tương đương `key=value`|
|sử dụng dấu `#` để viết comment cho cặp `key=value`|`# your comment`|
|những dòng sẽ bị bỏ qua khi bắt đầu với những ký tự sau |`khoảng trắng`, dấu `!`, và dấu `#`|
|có thể `add` trùng `key`, tuy nhiên `Properties` class chỉ lấy`value` của `key` cuối cùng, <br />do `Properties` class sử dụng `Map` interface để lưu trữ dữ liệu, nên cặp `key=value` cuối cùng được giữ lại||
|`value` có thể kéo dài vài dòng, nếu cuối mỗi dòng kết thúc bằng dấu `\` |`targetCities=\`<br />`Detroit,\`<br />`Chicago,\`<br />`Los Angeles`|
|những ký tự có thể sử dụng trong file `.properties`|`\n`, `\r`, `\t`|
|để sử dụng ký tự gạch chéo ngược `\`, thêm ký tự gạch chéo ngược phía trước| `\\`|

________________________________________________________________________________




