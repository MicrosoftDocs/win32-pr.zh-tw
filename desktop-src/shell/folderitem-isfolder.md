---
description: 指出專案是否為資料夾。
ms.assetid: fb080c8f-04b1-4f9a-9219-0951a2e950ea
title: 'FolderItem. IsFolder 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bf0bd4eb9b7964620fe705d6e8f4d10644ca234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971900"
---
# <a name="folderitemisfolder-property"></a><span data-ttu-id="5c627-103">FolderItem. IsFolder 屬性</span><span class="sxs-lookup"><span data-stu-id="5c627-103">FolderItem.IsFolder property</span></span>

<span data-ttu-id="5c627-104">指出專案是否為資料夾。</span><span class="sxs-lookup"><span data-stu-id="5c627-104">Indicates if the item is a folder.</span></span>

<span data-ttu-id="5c627-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5c627-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c627-106">語法</span><span class="sxs-lookup"><span data-stu-id="5c627-106">Syntax</span></span>


```JScript
bIsFolder = FolderItem.IsFolder
```



## <a name="property-value"></a><span data-ttu-id="5c627-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="5c627-107">Property value</span></span>

<span data-ttu-id="5c627-108">如果專案是資料夾，則為收到 **true** 的 **布林值**; 如果不是，則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="5c627-108">A **Boolean** that receives **true** if the item is a folder or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="5c627-109">範例</span><span class="sxs-lookup"><span data-stu-id="5c627-109">Examples</span></span>

<span data-ttu-id="5c627-110">下列範例會使用 **IsFolder** 來判斷 Windows 目錄是否為資料夾。</span><span class="sxs-lookup"><span data-stu-id="5c627-110">The following example uses **IsFolder** to determine whether the Windows directory is a folder.</span></span> <span data-ttu-id="5c627-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="5c627-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5c627-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="5c627-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFolderJ()
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
                
                bReturn = objFolderItem.IsFolder;
            }
        }
    }
</script>
```



<span data-ttu-id="5c627-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="5c627-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFolderVB()
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
                                
                    bReturn = objFolderItem.IsFolder
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5c627-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="5c627-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFolderVB()
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
                    
                    bReturn = objFolderItem.IsFolder
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



## <a name="requirements"></a><span data-ttu-id="5c627-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c627-115">Requirements</span></span>



| <span data-ttu-id="5c627-116">需求</span><span class="sxs-lookup"><span data-stu-id="5c627-116">Requirement</span></span> | <span data-ttu-id="5c627-117">值</span><span class="sxs-lookup"><span data-stu-id="5c627-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c627-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c627-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5c627-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c627-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c627-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c627-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5c627-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c627-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5c627-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5c627-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c627-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c627-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5c627-124">Idl</span><span class="sxs-lookup"><span data-stu-id="5c627-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c627-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c627-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5c627-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5c627-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c627-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="5c627-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




