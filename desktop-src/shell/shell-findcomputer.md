---
描述： FindComputer 方法-' 顯示搜尋結果：電腦對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。
assetid： 0304b955-afde-4de4-824a-9ec9c9530360 title： FindComputer 方法 (Shldisp. h) ms. 主題： reference ms. date： 05/31/2018 topic_type： 
- APIRef
- kbSyntax api_name： 
- Shell. FindComputer api_type： 
- COM api_location： 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>FindComputer 方法

顯示 [ **搜尋結果：電腦** ] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。

## <a name="syntax"></a>語法


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="examples"></a>範例

下列範例顯示使用中的 **FindComputer** 。 此程式碼的結果與按下 [ **開始** ] 按鈕、按一下 [ **搜尋**]、按一下 [ **印表機]、[電腦] 或 [人員** ] 選項，然後按一下 **網路上的電腦** 一樣。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
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
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




