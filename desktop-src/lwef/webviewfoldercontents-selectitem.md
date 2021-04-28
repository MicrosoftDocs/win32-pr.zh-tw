---
title: 'WebViewFolderContents. SelectItem 方法 (Shldisp .h) '
description: WebViewFolderContents. SelectItem 方法-在 view 中設定專案的選取狀態。
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- SelectItem 方法舊版 Windows 環境功能
- SelectItem 方法舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，SelectItem 方法
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66e2d05c010199f05826df7ed4591e8c7c1723e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102607"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="e90c1-106">WebViewFolderContents. SelectItem 方法</span><span class="sxs-lookup"><span data-stu-id="e90c1-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="e90c1-107">在視圖中設定專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="e90c1-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="e90c1-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="e90c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="e90c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90c1-110">*vItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e90c1-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90c1-111">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="e90c1-111">Type: **Variant\***</span></span>

<span data-ttu-id="e90c1-112">將設定選取狀態的 [**FolderItem**](../shell/folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e90c1-112">The [**FolderItem**](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="e90c1-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e90c1-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90c1-114">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="e90c1-114">Type: **Integer**</span></span>

<span data-ttu-id="e90c1-115">一組旗標，表示新的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="e90c1-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="e90c1-116">這可以是下列其中一個或多個值。</span><span class="sxs-lookup"><span data-stu-id="e90c1-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="e90c1-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="e90c1-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e90c1-118">取消選取專案。</span><span class="sxs-lookup"><span data-stu-id="e90c1-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="e90c1-119">(1)</span><span class="sxs-lookup"><span data-stu-id="e90c1-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e90c1-120">選取專案。</span><span class="sxs-lookup"><span data-stu-id="e90c1-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="e90c1-121">(3)</span><span class="sxs-lookup"><span data-stu-id="e90c1-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e90c1-122">將專案放在編輯模式中。</span><span class="sxs-lookup"><span data-stu-id="e90c1-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="e90c1-123">(4)</span><span class="sxs-lookup"><span data-stu-id="e90c1-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e90c1-124">取消選取指定的專案以外的所有專案。</span><span class="sxs-lookup"><span data-stu-id="e90c1-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="e90c1-125">(8)</span><span class="sxs-lookup"><span data-stu-id="e90c1-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e90c1-126">確定專案顯示在視圖中。</span><span class="sxs-lookup"><span data-stu-id="e90c1-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="e90c1-127">(16)</span><span class="sxs-lookup"><span data-stu-id="e90c1-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e90c1-128">將焦點提供給專案。</span><span class="sxs-lookup"><span data-stu-id="e90c1-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90c1-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="e90c1-129">Return value</span></span>

<span data-ttu-id="e90c1-130">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e90c1-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e90c1-131">範例</span><span class="sxs-lookup"><span data-stu-id="e90c1-131">Examples</span></span>

<span data-ttu-id="e90c1-132">下列範例會針對內嵌于 HTML 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="e90c1-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="e90c1-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e90c1-133">Requirements</span></span>



| <span data-ttu-id="e90c1-134">需求</span><span class="sxs-lookup"><span data-stu-id="e90c1-134">Requirement</span></span> | <span data-ttu-id="e90c1-135">值</span><span class="sxs-lookup"><span data-stu-id="e90c1-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90c1-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e90c1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e90c1-137">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e90c1-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e90c1-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e90c1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e90c1-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e90c1-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e90c1-140">標頭</span><span class="sxs-lookup"><span data-stu-id="e90c1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90c1-141"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e90c1-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e90c1-142">Idl</span><span class="sxs-lookup"><span data-stu-id="e90c1-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e90c1-143"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e90c1-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e90c1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e90c1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90c1-145"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e90c1-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

