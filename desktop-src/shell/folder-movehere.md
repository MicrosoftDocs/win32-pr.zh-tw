---
description: 將專案或專案移至此資料夾。
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: 'MoveHere 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: eb826d23a168d81d838341e96fa5e613f8b6f5261a3cda548a2be320acebbde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458916"
---
# <a name="foldermovehere-method"></a>MoveHere 方法

將專案或專案移至此資料夾。

## <a name="syntax"></a>語法


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* \[在\]
</dt> <dd>

類型： **Variant**

要移動的專案。 這可以是代表檔案名、 [**FolderItem**](folderitem.md) 物件或 [**FolderItems**](folderitems.md) 物件的字串。

</dd> <dt>

*vOptions* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

移動操作的選項。 這個值可以是零或下列值的組合。 這些值是根據定義來與 c + + [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa)結構的 **fFlags** 成員搭配使用的旗標。 這些旗標並未定義為 Visual Basic、VBScript 或 JScript 的定義，因此您必須自行定義它們或使用其對等數值。

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



  (9182) 


</dt> <dd>

[版本5.0。](versions.md) 請勿將連接的檔案移動為群組。 只移動指定的檔案。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 並非所有的方法都會針對所有資料夾執行。 例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。 如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。

 

## <a name="examples"></a>範例

下列範例會使用 **MoveHere** 將檔案 Temp.txt 從 c 磁片磁碟機的根目錄移至 c： \\ Windows 資料夾。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
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



 

 




