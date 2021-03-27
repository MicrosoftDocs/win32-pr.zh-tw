---
description: 包含資料夾的離線狀態。
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: 'Folder2. OfflineStatus 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971908"
---
# <a name="folder2offlinestatus-property"></a>Folder2. OfflineStatus 屬性

包含資料夾的離線狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>屬性值

設定為下列其中一個值的 **整數** 。

<dt>



  (.OFS \_ DIRTYCACHE) 


</dt> <dd>

伺服器在線上，有未同步處理的變更。

</dd> <dt>



  (.OFS \_ 非使用中) 


</dt> <dd>

未啟用此資料夾的離線快取。

</dd> <dt>



  (.OFS \_ 離線) 


</dt> <dd>

伺服器已離線。

</dd> <dt>



  (.OFS \_ ONLINE) 


</dt> <dd>

伺服器在線上。

</dd> <dt>



  (.OFS \_ SERVERBACK) 


</dt> <dd>

伺服器已離線，但可達到。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> 離線檔案必須透過資料夾選項啟用， **OfflineStatus** 才能正確運作。 如果未啟用離線檔案選項，屬性會傳回 **\_ 非** 使用中的 .ofs。

 

## <a name="examples"></a>範例

下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **OfflineStatus** 。

Jscript：


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Folder2**](folder2-object.md)
</dt> <dt>

[**資料夾**](folder.md)
</dt> </dl>

 

 




