---
description: 決定輸入面板是否已準備好顯示自動完成清單。
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'ITipAutocompleteClient：： RequestShowUI 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193151"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="114d5-103">ITipAutocompleteClient：： RequestShowUI 方法</span><span class="sxs-lookup"><span data-stu-id="114d5-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="114d5-104">決定輸入面板是否已準備好顯示自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="114d5-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="114d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="114d5-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="114d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="114d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114d5-107">*hWndACList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="114d5-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114d5-108">自動完成清單使用者介面的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="114d5-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="114d5-109">*pfAllowShowing* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="114d5-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="114d5-110">如果用戶端建議不要顯示自動完成清單使用者介面，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="114d5-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="114d5-111">如果自動完成提供者可以顯示清單使用者介面，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="114d5-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114d5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="114d5-112">Return value</span></span>

<span data-ttu-id="114d5-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="114d5-113">This method can return one of these values.</span></span>



| <span data-ttu-id="114d5-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="114d5-114">Return code</span></span>                                                                            | <span data-ttu-id="114d5-115">Description</span><span class="sxs-lookup"><span data-stu-id="114d5-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="114d5-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="114d5-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="114d5-117">成功。</span><span class="sxs-lookup"><span data-stu-id="114d5-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="114d5-118"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="114d5-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="114d5-119">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="114d5-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="114d5-120">備註</span><span class="sxs-lookup"><span data-stu-id="114d5-120">Remarks</span></span>

<span data-ttu-id="114d5-121">當自動完成提供者即將顯示自動完成使用者介面時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="114d5-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="114d5-122">如果用戶端的內部狀態不允許提供者顯示使用者介面， *pfAllowShowing* 會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="114d5-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="114d5-123">例如，當文字從 Tablet PC 輸入面板上的手寫面板傳送至欄位，且使用者立即開始筆墨時，用戶端將不會建議顯示自動完成使用者介面，藉由將 *pfAllowShowing* 設定為 **FALSE**，以避免 destructing 使用者的筆跡。</span><span class="sxs-lookup"><span data-stu-id="114d5-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="114d5-124">呼叫 **RequestShowUI** ，在呼叫 [**ITipAutocompleteClient：:P referredrects 方法**](itipautocompleteclient-preferredrects.md)之前，先設定 popup 自動完成清單視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="114d5-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="114d5-125">若未這麼做，將會在呼叫 **PreferredRects** 時造成 **E \_ INVALIDARG** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="114d5-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="114d5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="114d5-126">Requirements</span></span>



| <span data-ttu-id="114d5-127">需求</span><span class="sxs-lookup"><span data-stu-id="114d5-127">Requirement</span></span> | <span data-ttu-id="114d5-128">值</span><span class="sxs-lookup"><span data-stu-id="114d5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114d5-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="114d5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="114d5-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="114d5-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="114d5-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="114d5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="114d5-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="114d5-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="114d5-133">標頭</span><span class="sxs-lookup"><span data-stu-id="114d5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="114d5-134"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="114d5-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="114d5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="114d5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="114d5-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="114d5-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="114d5-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="114d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114d5-138">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="114d5-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="114d5-139">**ITipAutocompleteClient：:P referredRects 方法**</span><span class="sxs-lookup"><span data-stu-id="114d5-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="114d5-140">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="114d5-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




