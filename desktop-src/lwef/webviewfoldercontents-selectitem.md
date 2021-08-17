---
title: 'WebViewFolderContents. SelectItem 方法 (Shldisp .h) '
description: WebViewFolderContents. SelectItem 方法-在 view 中設定專案的選取狀態。
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- SelectItem 方法舊版 Windows 環境功能
- SelectItem 方法舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，SelectItem 方法
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d144801e62962f4071b6c8e60147326908a9b4f7787e0d4ac549be9c51fa3c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960618"
---
# <a name="webviewfoldercontentsselectitem-method"></a>WebViewFolderContents. SelectItem 方法

在視圖中設定專案的選取狀態。

## <a name="syntax"></a>語法


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* \[在\]
</dt> <dd>

類型： **Variant \***

將設定選取狀態的 [**FolderItem**](../shell/folderitem.md) 物件。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

類型： **整數**

一組旗標，表示新的選取狀態。 這可以是下列其中一個或多個值。

<dt>



  (0)


</dt> <dd>

取消選取專案。

</dd> <dt>



 (1)


</dt> <dd>

選取專案。

</dd> <dt>



 (3)


</dt> <dd>

將專案放在編輯模式中。

</dd> <dt>



 (4)


</dt> <dd>

取消選取指定的專案以外的所有專案。

</dd> <dt>



 (8)


</dt> <dd>

確定專案顯示在視圖中。

</dd> <dt>



 (16)


</dt> <dd>

將焦點提供給專案。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="examples"></a>範例

下列範例示範如何適當地使用此方法，以供 HTML 中內嵌 JScript。


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

