---
description: 顯示或隱藏自動完成清單。
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'ITipAutocompleteProvider：： Show 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695184"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="88887-103">ITipAutocompleteProvider：： Show 方法</span><span class="sxs-lookup"><span data-stu-id="88887-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="88887-104">顯示或隱藏自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="88887-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="88887-105">語法</span><span class="sxs-lookup"><span data-stu-id="88887-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="88887-106">參數</span><span class="sxs-lookup"><span data-stu-id="88887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88887-107">*fShow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="88887-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88887-108">**TRUE** 表示顯示自動完成使用者介面， **FALSE** 則會隱藏自動完成清單使用者介面。</span><span class="sxs-lookup"><span data-stu-id="88887-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88887-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="88887-109">Return value</span></span>

<span data-ttu-id="88887-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="88887-110">This method can return one of these values.</span></span>



| <span data-ttu-id="88887-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="88887-111">Return code</span></span>                                                                            | <span data-ttu-id="88887-112">Description</span><span class="sxs-lookup"><span data-stu-id="88887-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="88887-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="88887-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="88887-114">成功。</span><span class="sxs-lookup"><span data-stu-id="88887-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="88887-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="88887-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="88887-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="88887-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88887-117">備註</span><span class="sxs-lookup"><span data-stu-id="88887-117">Remarks</span></span>

<span data-ttu-id="88887-118">用戶端會呼叫這個方法來顯示或隱藏自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="88887-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="88887-119">如果未顯示自動完成清單，且 *fShow* 為 **FALSE**，則這個方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="88887-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="88887-120">如果顯示自動完成清單，且 *fShow* 為 **TRUE**，則這個方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="88887-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="88887-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="88887-121">Requirements</span></span>



| <span data-ttu-id="88887-122">需求</span><span class="sxs-lookup"><span data-stu-id="88887-122">Requirement</span></span> | <span data-ttu-id="88887-123">值</span><span class="sxs-lookup"><span data-stu-id="88887-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88887-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88887-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88887-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88887-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="88887-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88887-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88887-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="88887-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="88887-128">標頭</span><span class="sxs-lookup"><span data-stu-id="88887-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="88887-129"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="88887-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88887-130">DLL</span><span class="sxs-lookup"><span data-stu-id="88887-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88887-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88887-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="88887-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88887-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88887-133">**ITipAutocompleteProvider 介面**</span><span class="sxs-lookup"><span data-stu-id="88887-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="88887-134">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="88887-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




