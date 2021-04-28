---
description: FolderItemVerbs： Count 屬性-包含集合中的專案數。
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: 'FolderItemVerbs： Count 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5545ea64da914188226fbdabf7cc6301baa695af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089546"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="8ba62-103">FolderItemVerbs Count 屬性</span><span class="sxs-lookup"><span data-stu-id="8ba62-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="8ba62-104">包含集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="8ba62-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="8ba62-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8ba62-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba62-106">語法</span><span class="sxs-lookup"><span data-stu-id="8ba62-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="8ba62-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="8ba62-107">Property value</span></span>

<span data-ttu-id="8ba62-108">接收 **Count** 屬性的 **整數**。</span><span class="sxs-lookup"><span data-stu-id="8ba62-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="8ba62-109">範例</span><span class="sxs-lookup"><span data-stu-id="8ba62-109">Examples</span></span>

<span data-ttu-id="8ba62-110">下列範例會使用 **Count** 來取得主控台資料夾的可用動詞計數。</span><span class="sxs-lookup"><span data-stu-id="8ba62-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="8ba62-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="8ba62-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8ba62-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="8ba62-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="8ba62-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="8ba62-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
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
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8ba62-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="8ba62-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
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
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8ba62-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ba62-115">Requirements</span></span>



| <span data-ttu-id="8ba62-116">需求</span><span class="sxs-lookup"><span data-stu-id="8ba62-116">Requirement</span></span> | <span data-ttu-id="8ba62-117">值</span><span class="sxs-lookup"><span data-stu-id="8ba62-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba62-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ba62-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba62-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ba62-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ba62-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ba62-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba62-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ba62-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ba62-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8ba62-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ba62-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba62-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8ba62-124">Idl</span><span class="sxs-lookup"><span data-stu-id="8ba62-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ba62-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ba62-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8ba62-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8ba62-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba62-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8ba62-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




