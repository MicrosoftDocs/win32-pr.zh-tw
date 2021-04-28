---
描述： IShellDispatch. FindComputer 方法-' 顯示搜尋結果：電腦對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。
assetid： 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title： IShellDispatch. FindComputer 方法 (Shldisp .h) ms. 主題： reference ms. date： 05/31/2018 topic_type： 
- APIRef
- kbSyntax api_name： 
- IShellDispatch. FindComputer api_type： 
- COM api_location： 
- Shell32.dll
---

# <a name="ishelldispatchfindcomputer-method"></a>IShellDispatch. FindComputer 方法

顯示 [ **搜尋結果：電腦** ] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。

## <a name="syntax"></a>語法


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法是透過 [**FindComputer**](shell-findcomputer.md) 方法來執行和存取。

## <a name="examples"></a>範例

下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **FindComputer** 。

Jscript：


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



VBScript


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

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



 

 




