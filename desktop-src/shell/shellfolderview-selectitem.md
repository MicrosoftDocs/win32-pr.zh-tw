---
description: ShellFolderView. SelectItem 方法-在 view 中設定專案的選取狀態。
title: 'ShellFolderView. SelectItem 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: ab0f65094f638c56df6a10434f9a404072278c55
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842549"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="a9f95-103">ShellFolderView. SelectItem 方法</span><span class="sxs-lookup"><span data-stu-id="a9f95-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="a9f95-104">在視圖中設定專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f95-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f95-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9f95-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="a9f95-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f95-107">*vItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9f95-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f95-108">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="a9f95-108">Type: **Variant\***</span></span>

<span data-ttu-id="a9f95-109">將設定選取狀態的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a9f95-109">The [**FolderItem**](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="a9f95-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9f95-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f95-111">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="a9f95-111">Type: **Integer**</span></span>

<span data-ttu-id="a9f95-112">一組旗標，表示新的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f95-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="a9f95-113">這可以是下列其中一個或多個值。</span><span class="sxs-lookup"><span data-stu-id="a9f95-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="a9f95-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="a9f95-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a9f95-115">取消選取專案。</span><span class="sxs-lookup"><span data-stu-id="a9f95-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="a9f95-116">(1)</span><span class="sxs-lookup"><span data-stu-id="a9f95-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a9f95-117">選取專案。</span><span class="sxs-lookup"><span data-stu-id="a9f95-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="a9f95-118">(3)</span><span class="sxs-lookup"><span data-stu-id="a9f95-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a9f95-119">將專案放在編輯模式中。</span><span class="sxs-lookup"><span data-stu-id="a9f95-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="a9f95-120">(4)</span><span class="sxs-lookup"><span data-stu-id="a9f95-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a9f95-121">取消選取指定的專案以外的所有專案。</span><span class="sxs-lookup"><span data-stu-id="a9f95-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="a9f95-122">(8)</span><span class="sxs-lookup"><span data-stu-id="a9f95-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a9f95-123">確定專案顯示在視圖中。</span><span class="sxs-lookup"><span data-stu-id="a9f95-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="a9f95-124">(16)</span><span class="sxs-lookup"><span data-stu-id="a9f95-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a9f95-125">將焦點提供給專案。</span><span class="sxs-lookup"><span data-stu-id="a9f95-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f95-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9f95-126">Return value</span></span>

<span data-ttu-id="a9f95-127">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a9f95-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9f95-128">備註</span><span class="sxs-lookup"><span data-stu-id="a9f95-128">Remarks</span></span>

<span data-ttu-id="a9f95-129">[**FocusedItem**](shellfolderview-focuseditem.md) 只能在本機系統上呼叫。</span><span class="sxs-lookup"><span data-stu-id="a9f95-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="a9f95-130">當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。</span><span class="sxs-lookup"><span data-stu-id="a9f95-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="a9f95-131">範例</span><span class="sxs-lookup"><span data-stu-id="a9f95-131">Examples</span></span>

<span data-ttu-id="a9f95-132">下列範例示範如何在內嵌于 HTML 的 JScript 中正確使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="a9f95-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="a9f95-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9f95-133">Requirements</span></span>



| <span data-ttu-id="a9f95-134">需求</span><span class="sxs-lookup"><span data-stu-id="a9f95-134">Requirement</span></span> | <span data-ttu-id="a9f95-135">值</span><span class="sxs-lookup"><span data-stu-id="a9f95-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f95-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9f95-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f95-137">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9f95-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a9f95-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9f95-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f95-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9f95-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a9f95-140">標頭</span><span class="sxs-lookup"><span data-stu-id="a9f95-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9f95-141"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f95-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a9f95-142">Idl</span><span class="sxs-lookup"><span data-stu-id="a9f95-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9f95-143"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9f95-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a9f95-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a9f95-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9f95-145"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a9f95-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




