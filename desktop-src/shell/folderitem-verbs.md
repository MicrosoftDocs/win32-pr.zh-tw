---
description: 抓取專案的 FolderItemVerbs 物件。 此物件是可以在專案上執行的動詞集合。
ms.assetid: e31160cd-093a-45a6-a066-58120c44eb2c
title: 'FolderItem (Shldisp 的動詞方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f15c2471f749748f7928a45aa03037d955c75d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111725"
---
# <a name="folderitemverbs-method"></a><span data-ttu-id="90932-104">FolderItem 動詞方法</span><span class="sxs-lookup"><span data-stu-id="90932-104">FolderItem.Verbs method</span></span>

<span data-ttu-id="90932-105">抓取專案的 [**FolderItemVerbs**](folderitemverbs.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="90932-105">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="90932-106">此物件是可以在專案上執行的動詞集合。</span><span class="sxs-lookup"><span data-stu-id="90932-106">This object is the collection of verbs that can be executed on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="90932-107">語法</span><span class="sxs-lookup"><span data-stu-id="90932-107">Syntax</span></span>


```JScript
retVal = FolderItem.Verbs()
```



## <a name="parameters"></a><span data-ttu-id="90932-108">參數</span><span class="sxs-lookup"><span data-stu-id="90932-108">Parameters</span></span>

<span data-ttu-id="90932-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="90932-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90932-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="90932-110">Return value</span></span>

<span data-ttu-id="90932-111">類型： **[ **FolderItemVerbs**](folderitemverbs.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="90932-111">Type: **[**FolderItemVerbs**](folderitemverbs.md)\*\***</span></span>

<span data-ttu-id="90932-112">[**FolderItemVerbs**](folderitemverbs.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="90932-112">An object reference to the [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="90932-113">範例</span><span class="sxs-lookup"><span data-stu-id="90932-113">Examples</span></span>

<span data-ttu-id="90932-114">下列範例會使用 **動詞** 來抓取 [**FolderItemVerbs**](folderitemverbs.md) 物件，此物件代表可在 Windows 資料夾上執行的一組動詞。</span><span class="sxs-lookup"><span data-stu-id="90932-114">The following example uses **Verbs** to retrieve the [**FolderItemVerbs**](folderitemverbs.md) object representing the set of verbs that can be executed on the Windows folder.</span></span> <span data-ttu-id="90932-115">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="90932-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="90932-116">Jscript：</span><span class="sxs-lookup"><span data-stu-id="90932-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsJ()
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
                var objItemVerbs;
                
                objItemVerbs = objFolderItem.Verbs();
                if (objItemVerbs != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="90932-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="90932-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsVB()
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
                    dim objItemVerbs
                    
                    set objItemVerbs = objFolderItem.Verbs
                        if (not objItemVerbs is nothing) then
                            'Add code here
                        end if
                    set objItemVerbs = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="90932-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="90932-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsVB()
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
                    Dim objItemVerbs As FolderItemVerbs
                    
                    Set objItemVerbs = objFolderItem.Verbs
                        If (Not objItemVerbs Is Nothing) Then
                            'Add code here
                        End If
                    Set objItemVerbs = Nothing
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



## <a name="requirements"></a><span data-ttu-id="90932-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="90932-119">Requirements</span></span>



| <span data-ttu-id="90932-120">需求</span><span class="sxs-lookup"><span data-stu-id="90932-120">Requirement</span></span> | <span data-ttu-id="90932-121">值</span><span class="sxs-lookup"><span data-stu-id="90932-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90932-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90932-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90932-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90932-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="90932-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90932-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90932-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90932-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="90932-126">標頭</span><span class="sxs-lookup"><span data-stu-id="90932-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="90932-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="90932-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="90932-128">Idl</span><span class="sxs-lookup"><span data-stu-id="90932-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90932-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="90932-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="90932-130">DLL</span><span class="sxs-lookup"><span data-stu-id="90932-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90932-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="90932-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90932-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90932-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90932-133">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="90932-133">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="90932-134">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="90932-134">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> <dt>

[<span data-ttu-id="90932-135">**Doit r**</span><span class="sxs-lookup"><span data-stu-id="90932-135">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




