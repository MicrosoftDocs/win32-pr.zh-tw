---
description: 由自動完成用戶端用來通知應用程式使用者已筆跡輸入面板中的文字。
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'ITipAutocompleteProvider：： UpdatePendingText 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027548"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="bfa69-103">ITipAutocompleteProvider：： UpdatePendingText 方法</span><span class="sxs-lookup"><span data-stu-id="bfa69-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="bfa69-104">由自動完成用戶端用來通知應用程式使用者已筆跡輸入面板中的文字。</span><span class="sxs-lookup"><span data-stu-id="bfa69-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa69-105">語法</span><span class="sxs-lookup"><span data-stu-id="bfa69-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="bfa69-106">參數</span><span class="sxs-lookup"><span data-stu-id="bfa69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa69-107">*bstrPendingText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfa69-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa69-108">要用來產生自動完成清單的來源文字。</span><span class="sxs-lookup"><span data-stu-id="bfa69-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa69-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfa69-109">Return value</span></span>

<span data-ttu-id="bfa69-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bfa69-110">This method can return one of these values.</span></span>



| <span data-ttu-id="bfa69-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bfa69-111">Return code</span></span>                                                                            | <span data-ttu-id="bfa69-112">Description</span><span class="sxs-lookup"><span data-stu-id="bfa69-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bfa69-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa69-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="bfa69-114">成功。</span><span class="sxs-lookup"><span data-stu-id="bfa69-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="bfa69-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa69-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="bfa69-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bfa69-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfa69-117">備註</span><span class="sxs-lookup"><span data-stu-id="bfa69-117">Remarks</span></span>

<span data-ttu-id="bfa69-118">此文字不會包含已在焦點欄位中插入的文字。</span><span class="sxs-lookup"><span data-stu-id="bfa69-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="bfa69-119">自動完成提供者負責將目前的欄位文字和選取範圍納入考慮，以產生自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="bfa69-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="bfa69-120">當 *bstrPendingText* 為 **Null** 時，就會使用欄位中選取範圍的目前文字來產生自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="bfa69-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa69-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfa69-121">Requirements</span></span>



| <span data-ttu-id="bfa69-122">需求</span><span class="sxs-lookup"><span data-stu-id="bfa69-122">Requirement</span></span> | <span data-ttu-id="bfa69-123">值</span><span class="sxs-lookup"><span data-stu-id="bfa69-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa69-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfa69-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa69-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfa69-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="bfa69-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfa69-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa69-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="bfa69-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="bfa69-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bfa69-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa69-129"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="bfa69-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bfa69-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa69-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa69-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfa69-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="bfa69-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfa69-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa69-133">**ITipAutocompleteProvider 介面**</span><span class="sxs-lookup"><span data-stu-id="bfa69-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="bfa69-134">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="bfa69-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




