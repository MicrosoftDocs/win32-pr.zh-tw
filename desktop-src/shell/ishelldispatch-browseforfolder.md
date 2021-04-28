---
description: IShellDispatch. BrowseForFolder 方法-建立一個對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾資料夾物件。
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: 'IShellDispatch. BrowseForFolder 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ee6202c7029e2c27684e15d96dd6c38680cb0678
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086686"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>IShellDispatch. BrowseForFolder 方法

建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 [**資料夾**](folder.md) 物件。

## <a name="syntax"></a>語法


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>參數

<dl> <dt>

*Hwnd* \[在\]
</dt> <dd>

類型： **整數**

對話方塊的父視窗控制碼。 此值可以是零。

</dd> <dt>

*sTitle* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

表示在 [**流覽**] 對話方塊中顯示之標題的 **字串** 值。

</dd> <dt>

*microsoft.extensions.options.ioptions* \[在\]
</dt> <dd>

類型： **整數**

**整數** 值，其中包含方法的選項。 這可以是零或 [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)結構的 **ulFlags** 成員下所列的值組合。

</dd> <dt>

*vRootFolder* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

要在對話方塊中使用的根資料夾。 使用者無法在樹狀結構中流覽高於此資料夾的位置。 如果未指定此值，對話方塊中使用的根資料夾就是桌面。 這個值可以是指定資料夾路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值的字串。 請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。 在這些情況下，必須在其位置使用數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型：**資料夾 \* \***

所選資料夾之 [**資料夾**](folder.md) 物件的物件參考。

### <a name="vb"></a>VB

類型：**資料夾 \* \***

所選資料夾之 [**資料夾**](folder.md) 物件的物件參考。

## <a name="remarks"></a>備註

這個方法是透過 [**BrowseForFolder**](shell-browseforfolder.md) 方法來執行和存取。

## <a name="examples"></a>範例

下列範例會使用 **BrowseForFolder** ，在 Windows 資料夾上顯示標題為 "Example" 的流覽視窗。 JScript、VBScript 和 Visual Basic 會顯示使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
