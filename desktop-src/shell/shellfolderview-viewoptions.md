---
description: 取得一組旗標，指出視圖的目前選項。
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: 'ShellFolderView. ViewOptions 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991719"
---
# <a name="shellfolderviewviewoptions-property"></a>ShellFolderView. ViewOptions 屬性

取得一組旗標，指出視圖的目前選項。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a>屬性值

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收 view options 物件。 包含下列一或多個值：

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_SHOWALLOBJECTS** (0x00000001) 


</dt> <dd>

[ **顯示所有** 檔案] 選項為啟用狀態。

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_SHOWEXTENSIONS** (0x00000002) 


</dt> <dd>

[ **隱藏已知檔案類型的副檔名** ] 選項已停用。

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_SHOWCOMPCOLOR** (0x00000008) 


</dt> <dd>

[ **顯示具有替代色彩的壓縮檔案和資料夾** ] 選項為啟用狀態。

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_SHOWSYSFILES** (0x00000020) 


</dt> <dd>

[不 **顯示隱藏** 的檔案] 選項已啟用。

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_WIN95CLASSIC** (0x00000040) 


</dt> <dd>

[ **傳統樣式** ] 選項已啟用。

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_DOUBLECLICKINWEBVIEW** (0x00000080) 


</dt> <dd>

**按兩下以開啟專案** 選項已啟用。

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_DESKTOPHTML** (0x00000200) 


</dt> <dd>

[ **Active Desktop – View As Web Page** ] 選項為 enabled。

</dd> </dl>

## <a name="remarks"></a>備註

[**FocusedItem**](shellfolderview-focuseditem.md) 只能在本機系統上呼叫。 當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。

## <a name="examples"></a>範例

下列範例示範如何在內嵌于 HTML 的 JScript 中正確使用這個方法。


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
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



 

 
