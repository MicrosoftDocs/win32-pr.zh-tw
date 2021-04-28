---
title: 'WebViewFolderContents. PopupItemMenu 方法 (Shldisp .h) '
description: WebViewFolderContents. PopupItemMenu 方法-為指定的專案建立快捷方式功能表，並傳回選取的命令字串。
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- PopupItemMenu 方法舊版 Windows 環境功能
- PopupItemMenu 方法舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，PopupItemMenu 方法
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102636"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>WebViewFolderContents. PopupItemMenu 方法

為指定的專案建立快捷方式功能表，並傳回選取的命令字串。

## <a name="syntax"></a>語法


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* \[在\]
</dt> <dd>

類型： **Variant**

將建立快捷方式功能表的 [**FolderItem**](../shell/folderitem.md) 物件。

</dd> <dt>

*vx* \[ in、optional\]
</dt> <dd>

類型： **Variant**

功能表的水準位置（以螢幕座標為單位）。

</dd> <dt>

*vy* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

功能表的垂直位置（以螢幕座標為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

當此方法傳回時，會包含命令字串。

## <a name="examples"></a>範例

下列範例示範如何適當地使用 **PopupItemMenu** 來內嵌于 HTML 中的 JScript。


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

