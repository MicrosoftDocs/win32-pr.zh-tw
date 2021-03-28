---
description: 指出專案是否可裝載于瀏覽器或 Windows 檔案總管框架內。
ms.assetid: 472e0906-9561-4390-a503-c5e490245ea0
title: 'FolderItem. IsBrowsable 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsBrowsable
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d7c5f7a9cbde54647c299646bb6350c3be6aa2a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386018"
---
# <a name="folderitemisbrowsable-property"></a><span data-ttu-id="e0c87-103">FolderItem. IsBrowsable 屬性</span><span class="sxs-lookup"><span data-stu-id="e0c87-103">FolderItem.IsBrowsable property</span></span>

<span data-ttu-id="e0c87-104">指出專案是否可裝載于瀏覽器或 Windows 檔案總管框架內。</span><span class="sxs-lookup"><span data-stu-id="e0c87-104">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span>

<span data-ttu-id="e0c87-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e0c87-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c87-106">語法</span><span class="sxs-lookup"><span data-stu-id="e0c87-106">Syntax</span></span>


```JScript
bIsBrowsable = FolderItem.IsBrowsable
```



## <a name="property-value"></a><span data-ttu-id="e0c87-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="e0c87-107">Property value</span></span>

<span data-ttu-id="e0c87-108">**布林值**，如果可以流覽專案則為 **true** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="e0c87-108">A **Boolean** that receives **true** if the item can be browsed or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="e0c87-109">範例</span><span class="sxs-lookup"><span data-stu-id="e0c87-109">Examples</span></span>

<span data-ttu-id="e0c87-110">下列範例會使用 **IsBrowsable** 來判斷 Windows 資料夾的可流覽狀態。</span><span class="sxs-lookup"><span data-stu-id="e0c87-110">The following example uses **IsBrowsable** to determine the browsable state of the Windows folder.</span></span> <span data-ttu-id="e0c87-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="e0c87-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e0c87-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="e0c87-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsBrowsableJ()
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
                
                bReturn = objFolderItem.IsBrowsable;
            }
        }
    }
</script>
```



<span data-ttu-id="e0c87-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="e0c87-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsBrowsableVB()
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
                                
                    bReturn = objFolderItem.IsBrowsable
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e0c87-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="e0c87-114">Visual Basic:</span></span>


```VB
Private Sub fnIsBrowsableVB()
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
                    
                    bReturn = objFolderItem.IsBrowsable
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



## <a name="requirements"></a><span data-ttu-id="e0c87-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0c87-115">Requirements</span></span>



| <span data-ttu-id="e0c87-116">需求</span><span class="sxs-lookup"><span data-stu-id="e0c87-116">Requirement</span></span> | <span data-ttu-id="e0c87-117">值</span><span class="sxs-lookup"><span data-stu-id="e0c87-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c87-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0c87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c87-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0c87-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e0c87-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0c87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c87-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0c87-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0c87-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e0c87-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c87-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c87-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e0c87-124">Idl</span><span class="sxs-lookup"><span data-stu-id="e0c87-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0c87-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0c87-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e0c87-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e0c87-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0c87-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e0c87-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




