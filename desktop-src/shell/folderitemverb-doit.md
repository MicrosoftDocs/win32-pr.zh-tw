---
description: 在與動詞相關聯的 FolderItem 上執行動詞。
ms.assetid: 92400fe9-e4d1-4bc9-b4ee-d2adaf38154f
title: 'FolderItemVerb. Doit r 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.DoIt
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0703b9403dfe9ff6600de68aaa710cd5a55c225a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971873"
---
# <a name="folderitemverbdoit-method"></a><span data-ttu-id="7c7dc-103">FolderItemVerb. Doit r 方法</span><span class="sxs-lookup"><span data-stu-id="7c7dc-103">FolderItemVerb.DoIt method</span></span>

<span data-ttu-id="7c7dc-104">在與動詞相關聯的 [**FolderItem**](folderitem.md) 上執行動詞。</span><span class="sxs-lookup"><span data-stu-id="7c7dc-104">Executes a verb on the [**FolderItem**](folderitem.md) associated with the verb.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c7dc-105">Syntax</span></span>


```JScript
FolderItemVerb.DoIt()
```



## <a name="parameters"></a><span data-ttu-id="7c7dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c7dc-106">Parameters</span></span>

<span data-ttu-id="7c7dc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7c7dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c7dc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c7dc-108">Return value</span></span>

<span data-ttu-id="7c7dc-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7c7dc-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7c7dc-110">範例</span><span class="sxs-lookup"><span data-stu-id="7c7dc-110">Examples</span></span>

<span data-ttu-id="7c7dc-111">下列範例會使用 **doit r** ，在使用者的程式資料夾回應的動詞集合中執行第一個動詞。</span><span class="sxs-lookup"><span data-stu-id="7c7dc-111">The following example uses **DoIt** to execute the first verb in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="7c7dc-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="7c7dc-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7c7dc-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="7c7dc-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbDoItJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                objVerbs.Item(0).DoIt();
            }
        }
    }
</script>
```



<span data-ttu-id="7c7dc-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="7c7dc-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbDoItVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        objVerbs.Item(0).DoIt
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="7c7dc-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="7c7dc-115">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbDoItVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                objVerbs.Item(0).DoIt
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7c7dc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c7dc-116">Requirements</span></span>



| <span data-ttu-id="7c7dc-117">需求</span><span class="sxs-lookup"><span data-stu-id="7c7dc-117">Requirement</span></span> | <span data-ttu-id="7c7dc-118">值</span><span class="sxs-lookup"><span data-stu-id="7c7dc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7dc-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c7dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c7dc-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c7dc-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7c7dc-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c7dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c7dc-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c7dc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c7dc-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7c7dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c7dc-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c7dc-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7c7dc-125">Idl</span><span class="sxs-lookup"><span data-stu-id="7c7dc-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c7dc-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c7dc-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7c7dc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7c7dc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c7dc-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7c7dc-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




