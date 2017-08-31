# 基于draft-js编写的富文本编辑器

## demo
```
npm install
npm run storybook
```
查看 http://localhost:6006/

## props
* className: 类名，会加到container
* height: 编辑区域高度，会直接放到style.height上面，default: 300px
* value: EditorState, 用于赋值
* onChange: Function, (editorState) => {},回传editorState
* onImageInsert: Function, 必传
```
@param {String} base64 被插入图片的base64编码
@param {Function} insertImage 插入图片的方法, 传参为要插入的图片的url
```
* imageSizeLimit: 图片大小限制，单位是Byte，如10M = 1024 * 1024 *10，默认为10M
* imageMIME: 图片支持的类型， default:['image/png', 'image/jpeg']