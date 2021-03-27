---
description: 指出專案是否為檔案系統的一部分。
ms.assetid: 321a2109-88b5-4a41-9a67-dab3e82e95d8
title: 'FolderItem. IsFileSystem 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFileSystem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 852f022e1c24fa24c158ee4eb68dca44e6f010a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971901"
---
# <a name="folderitemisfilesystem-property"></a><span data-ttu-id="a5d30-103">FolderItem. IsFileSystem 屬性</span><span class="sxs-lookup"><span data-stu-id="a5d30-103">FolderItem.IsFileSystem property</span></span>

<span data-ttu-id="a5d30-104">指出專案是否為檔案系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="a5d30-104">Indicates if the item is part of the file system.</span></span>

<span data-ttu-id="a5d30-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a5d30-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d30-106">語法</span><span class="sxs-lookup"><span data-stu-id="a5d30-106">Syntax</span></span>


```JScript
bIsFileSystem = FolderItem.IsFileSystem
```



## <a name="property-value"></a><span data-ttu-id="a5d30-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="a5d30-107">Property value</span></span>

<span data-ttu-id="a5d30-108">**布林值**，如果專案是檔案系統的一部分則為 **true** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="a5d30-108">A **Boolean** that receives **true** if the item is part of the file system or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="a5d30-109">範例</span><span class="sxs-lookup"><span data-stu-id="a5d30-109">Examples</span></span>

<span data-ttu-id="a5d30-110">下列範例會使用 **IsFileSystem** 來判斷 Windows 資料夾是否為檔案系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="a5d30-110">The following example uses **IsFileSystem** to determine whether the Windows folder is a part of the file system.</span></span> <span data-ttu-id="a5d30-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="a5d30-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a5d30-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="a5d30-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFileSystemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFileSystem;
            }
        }
    }
</script>
```



<span data-ttu-id="a5d30-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="a5d30-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFileSystemVB()
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
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFileSystem
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a5d30-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="a5d30-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFileSystemVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFileSystem
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a5d30-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5d30-115">Requirements</span></span>



| <span data-ttu-id="a5d30-116">需求</span><span class="sxs-lookup"><span data-stu-id="a5d30-116">Requirement</span></span> | <span data-ttu-id="a5d30-117">值</span><span class="sxs-lookup"><span data-stu-id="a5d30-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d30-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5d30-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d30-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5d30-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a5d30-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5d30-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d30-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5d30-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5d30-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a5d30-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d30-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d30-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a5d30-124">Idl</span><span class="sxs-lookup"><span data-stu-id="a5d30-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5d30-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5d30-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a5d30-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a5d30-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d30-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a5d30-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




