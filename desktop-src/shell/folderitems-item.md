---
description: 抓取集合中指定之專案的 FolderItem 物件。
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: 'FolderItems 專案方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e246a1ada6cdf9935ae2ce9f8ca2a0ae25ced8ea08db8e98fef59a8fbc66ef40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679472"
---
# <a name="folderitemsitem-method"></a>FolderItems 專案方法

抓取集合中指定之專案的 [**FolderItem**](folderitem.md) 物件。

## <a name="syntax"></a>語法


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iIndex* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

要擷取之項目的索引，此索引以零起始。 這個值必須小於 [**Count**](folderitems-count.md) 屬性的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

[**FolderItem**](folderitem.md)物件的物件參考。

## <a name="examples"></a>範例

下列範例會使用 **專案** 來抓取 [**FolderItem**](folderitem.md)物件，代表 Windows 資料夾中找到的 Notepad.exe 檔案。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub fnFolderItemsItemVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FolderItems**](folderitems.md)
</dt> </dl>

 

 




