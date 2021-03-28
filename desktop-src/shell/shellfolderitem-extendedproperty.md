---
description: 從專案的屬性集取得屬性的值。 屬性可以依照名稱或屬性集的格式識別碼來指定 (FMTID) 和屬性識別碼 (PID) 。
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: 'ShellFolderItem. ExtendedProperty 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973592"
---
# <a name="shellfolderitemextendedproperty-method"></a>ShellFolderItem. ExtendedProperty 方法

從專案的屬性集取得屬性的值。 屬性可以依照名稱或屬性集的格式識別碼來指定 (FMTID) 和屬性識別碼 (PID) 。

## <a name="syntax"></a>語法


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sPropName* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

指定屬性的 **字串** 值。 如需詳細資訊，請參閱＜備註＞一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **Variant \** _

當此方法傳回時，會包含屬性的值（如果它存在於指定的專案中）。 此值將會有完整的輸入，例如，日期會以日期（而不是字串）的形式傳回。

如果屬性有效但不存在於指定的專案，則這個方法會傳回長度為零的字串，否則會傳回錯誤碼。

## <a name="remarks"></a>備註

有兩種方式可以指定屬性。 第一個是指派屬性的已知名稱，例如 "Author" 或 "Date"，以 _sPropName *。 不過，每個屬性都是元件物件模型 (COM) 屬性集的成員，也可以藉由指定其格式識別碼 (FMTID) 和屬性識別碼 (PID) 來識別。 [**FMTID**](../stg/structured-storage-serialized-property-set-format.md)是識別屬性集的 GUID，而 [**PID**](../stg/structured-storage-serialized-property-set-format.md)是識別屬性集內特定屬性的整數。

依 FMTID/PID 值指定屬性，通常比使用其名稱更有效率。 若要使用屬性的 FMTID/PID 值搭配 **ExtendedProperty**，必須將它們合併成 SCID。 SCID 是包含 FMTID/PID 值的字串，其格式為 "*FMTID * * pid*"，其中 FMTID 是屬性集 GUID 的字串形式。 例如，摘要資訊屬性集的作者屬性的 SCID 是 "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4"。

如需 Shell 目前支援的 FMTIDs 和 Pid 清單，請參閱 [**SHCOLUMNID**](./objects.md)。

## <a name="examples"></a>範例

此範例程式碼說明如何使用 **ExtendedProperty** 從 Word 檔取出 "Title" 和 "Author" 屬性。 一旦您有與檔案相關聯的 [**ShellFolderItem**](shellfolderitem-object.md) 物件，在此範例中， *fiWordDoc* 將其名稱傳遞給 **ExtendedProperty**，以抓取屬性的值。


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



更快速且更有效率的方法是將 SCID 傳遞至 **ExtendedProperty**。


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



下列範例會針對 JScript、VBScript 和 Visual Basic 示範此方法的適當用法。

Jscript：


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
