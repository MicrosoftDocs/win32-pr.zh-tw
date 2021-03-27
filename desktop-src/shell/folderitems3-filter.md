---
description: 設定萬用字元篩選器以套用至傳回的專案。
ms.assetid: 19ca82c5-16ff-46c7-8ea1-ddbfc2ce3ac9
title: 'FolderItems3： Filter 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Filter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26a24dc3ef1f4d0de09dbd97a5dce4c8ed8c783b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689247"
---
# <a name="folderitems3filter-method"></a><span data-ttu-id="f7ab1-103">FolderItems3. Filter 方法</span><span class="sxs-lookup"><span data-stu-id="f7ab1-103">FolderItems3.Filter method</span></span>

<span data-ttu-id="f7ab1-104">設定萬用字元篩選器以套用至傳回的專案。</span><span class="sxs-lookup"><span data-stu-id="f7ab1-104">Sets a wildcard filter to apply to the items returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ab1-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7ab1-105">Syntax</span></span>


```JScript
iRetVal = FolderItems3.Filter(
  grfFlags,
  bstrFilter
)
```



## <a name="parameters"></a><span data-ttu-id="f7ab1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7ab1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7ab1-107">*grfFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7ab1-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7ab1-108">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="f7ab1-108">Type: **Integer**</span></span>

<span data-ttu-id="f7ab1-109">此參數可以是 [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf)中所列的其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="f7ab1-109">This parameter can be one of the flags listed in [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span></span>

</dd> <dt>

<span data-ttu-id="f7ab1-110">*bstrFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7ab1-110">*bstrFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7ab1-111">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f7ab1-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f7ab1-112">指定應列在 [**FolderItems**](folderitems.md) 集合中之內容的篩選字串。</span><span class="sxs-lookup"><span data-stu-id="f7ab1-112">A filter string that specifies what should be listed in the [**FolderItems**](folderitems.md) collection.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f7ab1-113">範例</span><span class="sxs-lookup"><span data-stu-id="f7ab1-113">Examples</span></span>

<span data-ttu-id="f7ab1-114">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **篩選準則** 。</span><span class="sxs-lookup"><span data-stu-id="f7ab1-114">The following example shows the proper usage of **Filter** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f7ab1-115">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f7ab1-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems3FilterJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var SHCONTF_NONFOLDERS = 64;
                
                alert(objFolderItems3.Count);
                objFolderItems3.Filter(SHCONTF_NONFOLDERS, "*.txt");
                alert(objFolderItems3.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="f7ab1-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="f7ab1-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems3FilterVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim SHCONTF_NONFOLDERS
                
                    SHCONTF_NONFOLDERS = 64
                    alert(objFolderItems3.Count)
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.txt"
                    alert(objFolderItems3.Count)
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="f7ab1-117">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f7ab1-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems3FilterVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim SHCONTF_NONFOLDERS As Long
                    
                    SHCONTF_NONFOLDERS = 64
                    Debug.Print objFolderItems3.Count
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.exe"
                    Debug.Print objFolderItems3.Count
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f7ab1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7ab1-118">Requirements</span></span>



| <span data-ttu-id="f7ab1-119">需求</span><span class="sxs-lookup"><span data-stu-id="f7ab1-119">Requirement</span></span> | <span data-ttu-id="f7ab1-120">值</span><span class="sxs-lookup"><span data-stu-id="f7ab1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ab1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7ab1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ab1-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7ab1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7ab1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7ab1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ab1-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7ab1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f7ab1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f7ab1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7ab1-126"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7ab1-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f7ab1-127">Idl</span><span class="sxs-lookup"><span data-stu-id="f7ab1-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7ab1-128"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7ab1-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f7ab1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ab1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7ab1-130"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f7ab1-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ab1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7ab1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ab1-132">**FolderItems3**</span><span class="sxs-lookup"><span data-stu-id="f7ab1-132">**FolderItems3**</span></span>](folderitems3-object.md)
</dt> <dt>

[<span data-ttu-id="f7ab1-133">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="f7ab1-133">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="f7ab1-134">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="f7ab1-134">**FolderItem**</span></span>](folderitem.md)
</dt> </dl>

 

 
