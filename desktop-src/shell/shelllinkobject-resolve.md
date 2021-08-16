---
description: 尋找 Shell 連結的目標，即使目標已移動或重新命名也一樣。
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: 'ShellLinkObject 方法 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fdff3fd1a606b8dbec35476988497dd14892692a42e6502343716264873c184d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857491"
---
# <a name="shelllinkobjectresolve-method"></a>ShellLinkObject 方法

尋找 Shell 連結的目標，即使目標已移動或重新命名也一樣。

## <a name="syntax"></a>語法


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*fFlags* \[在\]
</dt> <dd>

類型： **整數**

指定要採取之動作的旗標。 這可以是下列值的組合：

<dt>



 (1)


</dt> <dd>

如果無法解析連結，請勿顯示對話方塊。 設定此旗標時， *fFlags* 的高序位字會指定超時時間（以毫秒為單位）。 如果在超時時間內無法解析連結，則此方法會傳回。 如果高序位字組設定為零，則超時期間預設為3000毫秒 (3 秒) 。

</dd> <dt>



 (4)


</dt> <dd>

如果連結已變更，請更新其路徑和識別碼清單。

</dd> <dt>



 (8)


</dt> <dd>

請勿更新連結資訊。

</dd> <dt>



 (16)


</dt> <dd>

請勿執行搜尋啟發學習法。

</dd> <dt>



  (32) 


</dt> <dd>

請勿使用分散式連結追蹤。

</dd> <dt>



 (64)


</dt> <dd>

停用分散式連結追蹤。 根據預設，分散式連結追蹤會根據磁片區名稱來追蹤多個裝置上的卸載式媒體。 它也會使用 UNC 路徑來追蹤磁碟機號已變更的遠端檔案系統。 設定此旗標會停用這兩種類型的追蹤。

</dd> <dt>



  (128) 


</dt> <dd>

呼叫 Windows Installer。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

這個方法基本上與要 [**解析**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)的功能完全相同。 如需連結解析的進一步討論，請參閱該頁面的 [備註] 區段。

## <a name="examples"></a>範例

下列範例會針對 JScript、VBScript 和 Visual Basic 顯示此方法的適當使用方式。

JScript：


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[只有 SP3 desktop 應用程式 Windows 2000 Professional\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
