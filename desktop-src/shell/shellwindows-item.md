---
description: 捕獲代表 Shell 視窗的 Microsoft-windows-ie-internetexplorer 物件。
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: 'ShellWindows 專案方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193161"
---
# <a name="shellwindowsitem-method"></a>ShellWindows 專案方法

捕獲代表 Shell 視窗的 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件。

## <a name="syntax"></a>語法


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iIndex* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

要擷取之項目的索引，此索引以零起始。 這個值必須小於 [**Count**](shellwindows-count.md) 屬性的值。 如果省略此值，則會使用預設值0。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

代表 Shell 視窗之 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件的物件參考。

## <a name="examples"></a>範例

下列範例會使用 [**專案**](folderitemverbs-item.md) 來取出代表第一個 Shell 視窗專案的 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Exdisp。h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
