---
description: 抓取資料夾中專案的詳細資料。 例如，其大小、類型或上次修改的時間。
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: 'GetDetailsOf 方法 (Shlobj.h \_ core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c703150069bc839f2d20024c0de8f3197fba09c5c3571e3de818dec3f3d6737c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860326"
---
# <a name="foldergetdetailsof-method"></a>GetDetailsOf 方法

抓取資料夾中專案的詳細資料。 例如，其大小、類型或上次修改的時間。

## <a name="syntax"></a>語法


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* 
</dt> <dd>

類型： **Variant**

要取得其資訊的專案。 這必須是 [**FolderItem**](folderitem.md) 物件。

</dd> <dt>

*iColumn* 
</dt> <dd>

類型： **整數**

**整數** 值，指定要取出的資訊。 專案的可用資訊取決於顯示它的資料夾。 此值會對應至顯示在 Shell 視圖中以零為基底的資料行編號。 針對檔案系統中的專案，這可以是下列其中一個值：

<dt>



  (0)


</dt> <dd>

抓取專案的名稱。

</dd> <dt>



 (1)


</dt> <dd>

捕獲專案的大小。

</dd> <dt>



 (2)


</dt> <dd>

抓取專案的型別。

</dd> <dt>



 (3)


</dt> <dd>

抓取專案上次修改的日期和時間。

</dd> <dt>



 (4)


</dt> <dd>

抓取專案的屬性。

</dd> <dt>



  (-1) 


</dt> <dd>

抓取專案的資訊提示資訊。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

包含已抓取詳細資料的字串。

## <a name="remarks"></a>備註

> [!Note]  
> 並非所有的方法都會針對所有資料夾執行。 例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。 如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。

 

## <a name="examples"></a>範例

下列範例會使用 **GetDetailsOf** 來取出名為 Clock.avi 之檔案的類型。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
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
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
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
| 標頭<br/>                   | <dl> <dt>Shlobj.h \_ core .h (包括 Shldisp) </dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
