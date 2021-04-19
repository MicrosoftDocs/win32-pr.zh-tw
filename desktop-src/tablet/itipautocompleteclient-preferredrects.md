---
description: 允許用戶端建議在何處放置自動完成清單，以避免重迭輸入面板。
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: 'ITipAutocompleteClient：:P referredRects 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984629"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="947a3-103">ITipAutocompleteClient：:P referredRects 方法</span><span class="sxs-lookup"><span data-stu-id="947a3-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="947a3-104">允許用戶端建議在何處放置自動完成清單，以避免重迭輸入面板。</span><span class="sxs-lookup"><span data-stu-id="947a3-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="947a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="947a3-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="947a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="947a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="947a3-107">*prcACList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="947a3-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="947a3-108">以螢幕座標表示提供者慣用位置和自動完成清單使用者介面大小的矩形。</span><span class="sxs-lookup"><span data-stu-id="947a3-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="947a3-109">*prcField* \[在\]</span><span class="sxs-lookup"><span data-stu-id="947a3-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="947a3-110">螢幕座標中的矩形，指出焦點欄位的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="947a3-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="947a3-111">*prcModified* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="947a3-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="947a3-112">以目前的提示狀態和慣用的自動完成清單位置和 *prcACList* 指定的大小為基礎的矩形。</span><span class="sxs-lookup"><span data-stu-id="947a3-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="947a3-113">*pfShownAboveTip* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="947a3-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="947a3-114">如果修改的矩形要顯示在文字輸入面板的目的地區域上方，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="947a3-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="947a3-115">在呼叫方法之前，必須將這個值初始化為提供者的慣用方向。</span><span class="sxs-lookup"><span data-stu-id="947a3-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="947a3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="947a3-116">Return value</span></span>

<span data-ttu-id="947a3-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="947a3-117">This method can return one of these values.</span></span>



| <span data-ttu-id="947a3-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="947a3-118">Return code</span></span>                                                                                  | <span data-ttu-id="947a3-119">Description</span><span class="sxs-lookup"><span data-stu-id="947a3-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="947a3-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="947a3-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="947a3-121">成功。</span><span class="sxs-lookup"><span data-stu-id="947a3-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="947a3-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="947a3-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="947a3-123">呼叫 [**ITipAutocompleteClient：： RequestShowUI 方法**](itipautocompleteclient-requestshowui.md) ，在呼叫 [**ITipAutocompleteClient：:P referredrects 方法**](itipautocompleteclient-preferredrects.md)之前，設定快顯視窗自動完成清單視窗。</span><span class="sxs-lookup"><span data-stu-id="947a3-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="947a3-124"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="947a3-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="947a3-125">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="947a3-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="947a3-126">備註</span><span class="sxs-lookup"><span data-stu-id="947a3-126">Remarks</span></span>

<span data-ttu-id="947a3-127">這是自動完成提供者在即將顯示自動完成使用者介面時所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="947a3-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="947a3-128">用戶端會修改 *prcACList* 透過 *prcModified* 引數所指定的提供者慣用矩形。</span><span class="sxs-lookup"><span data-stu-id="947a3-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="947a3-129">呼叫 [**ITipAutocompleteClient：： RequestShowUI 方法**](itipautocompleteclient-requestshowui.md) ，在呼叫 **PreferredRects** 之前，設定快顯自動完成清單視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="947a3-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="947a3-130">若未這麼做，將會在呼叫 **PreferredRects** 時造成 **E \_ INVALIDARG** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="947a3-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="947a3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="947a3-131">Requirements</span></span>



| <span data-ttu-id="947a3-132">需求</span><span class="sxs-lookup"><span data-stu-id="947a3-132">Requirement</span></span> | <span data-ttu-id="947a3-133">值</span><span class="sxs-lookup"><span data-stu-id="947a3-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="947a3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="947a3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="947a3-135">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="947a3-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="947a3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="947a3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="947a3-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="947a3-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="947a3-138">標頭</span><span class="sxs-lookup"><span data-stu-id="947a3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="947a3-139"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="947a3-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="947a3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="947a3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="947a3-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="947a3-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="947a3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="947a3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="947a3-143">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="947a3-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="947a3-144">**ITipAutocompleteClient：： RequestShowUI 方法**</span><span class="sxs-lookup"><span data-stu-id="947a3-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="947a3-145">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="947a3-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




