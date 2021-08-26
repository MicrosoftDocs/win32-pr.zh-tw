---
description: 將專案加入至 Microsoft Active Desktop。
title: 'ShellUIHelper. AddDesktopComponent 方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 5141b35b9fb71b09b9b269016d0b38cdb0b9f01ec88a02070a0f936934159930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941498"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>ShellUIHelper. AddDesktopComponent 方法

將專案加入至 Microsoft Active Desktop。

## <a name="syntax"></a>語法


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sURL* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

指定新的我的最愛專案之 URL 的 **字串** 值。

</dd> <dt>

*sType* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**字串** 值，指定要加入的專案類型。 這可以是下列其中一個值。

<dt>



  (映射) 


</dt> <dd>

元件為影像。

</dd> <dt>



  (網站) 


</dt> <dd>

元件是網站。

</dd> </dl> </dd> <dt>

*左方* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

元件左邊緣的位置，以螢幕座標為單位。

</dd> <dt>

*頂端* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

元件上邊緣的位置，以螢幕座標為單位。

</dd> <dt>

*寬度* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

元件的寬度（以螢幕單位為單位）。

</dd> <dt>

*高度* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

元件的高度，以螢幕單位為單位。

</dd> </dl>

## <a name="examples"></a>範例

下列範例會針對內嵌于 HTML 和 Visual Basic 的 JScript，顯示此方法的正確用法。

JScript：


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic：


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Exdisp。h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
