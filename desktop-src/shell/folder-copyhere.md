---
description: 將專案或專案複製到資料夾。
title: 'CopyHere 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991591"
---
# <a name="foldercopyhere-method"></a>CopyHere 方法

將專案或專案複製到資料夾。

## <a name="syntax"></a>語法


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* 
</dt> <dd>

類型： **Variant**

要複製的專案。 這可以是代表檔案名、 [**FolderItem**](folderitem.md) 物件或 [**FolderItems**](folderitems.md) 物件的字串。

</dd> <dt>

*vOptions* \[選\]
</dt> <dd>

類型： **Variant**

複製操作的選項。 這個值可以是零或下列值的組合。 這些值是根據定義來與 c + + [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa)結構的 **fFlags** 成員搭配使用的旗標。 每個 Shell 命名空間都必須提供自己的這些旗標執行，而且每個命名空間都可以選擇忽略部分或甚至所有的旗標。 這些旗標不是依 Visual Basic、VBScript 或 JScript 的名稱所定義，因此您必須自行定義，或使用其對等數值。

> [!Note]  
> 在某些情況下（例如壓縮的 ( .zip) 檔），設計可能會忽略某些選項旗標。

 

<dt>



 (4)


</dt> <dd>

不要顯示進度對話方塊。

</dd> <dt>



 (8)


</dt> <dd>

如果目標名稱的檔案已經存在，請將移動、複製或重新命名作業中的新名稱所要操作的檔案提供。

</dd> <dt>



 (16)


</dt> <dd>

針對顯示的任何對話方塊，回應 [全部是]。

</dd> <dt>



 (64)


</dt> <dd>

盡可能保留復原資訊。

</dd> <dt>



  (128) 


</dt> <dd>

只有在指定萬用字元檔案名 (時，才在檔案上執行操作。請 \* \*) 。

</dd> <dt>



  (256) 


</dt> <dd>

顯示 [進度] 對話方塊，但不顯示檔案名。

</dd> <dt>



  (512) 


</dt> <dd>

如果作業需要建立新的目錄，請不要確認建立該目錄。

</dd> <dt>



  (1024) 


</dt> <dd>

如果發生錯誤，則不顯示使用者介面。

</dd> <dt>



  (2048) 


</dt> <dd>

[版本4.71。](versions.md) 請勿複製檔案的安全性屬性。

</dd> <dt>



  (4096) 


</dt> <dd>

只能在本機目錄中操作。 請勿以遞迴方式操作子目錄。

</dd> <dt>



  (8192) 


</dt> <dd>

[版本5.0。](versions.md) 請勿將連接的檔案複製為群組。 只複製指定的檔案。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

呼叫程式未提供任何通知，以指出複製已完成。

> [!Note]  
> 並非所有的方法都會針對所有資料夾執行。 例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。 如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。

 

## <a name="examples"></a>範例

下列範例會使用 **CopyHere** 將 Autoexec.bat 檔案從根目錄複寫到 C： \\ Windows 目錄。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



VBScript


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料夾**](folder.md)
</dt> </dl>

 

 




