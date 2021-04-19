---
title: SendMessage 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 SendMessage 方法會將訊息傳送至線上商店的外掛程式。
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- sendMessage 方法 Windows Media Player
- sendMessage 方法 Windows Media Player、External 類別
- External class Windows Media Player，sendMessage 方法
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998402"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="c86b5-108">SendMessage 方法</span><span class="sxs-lookup"><span data-stu-id="c86b5-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="c86b5-109">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="c86b5-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c86b5-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="c86b5-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c86b5-111">**SendMessage** 方法會將訊息傳送至線上商店的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="c86b5-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86b5-112">語法</span><span class="sxs-lookup"><span data-stu-id="c86b5-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="c86b5-113">參數</span><span class="sxs-lookup"><span data-stu-id="c86b5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86b5-114">*Msg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c86b5-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86b5-115">包含訊息的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="c86b5-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="c86b5-116">*Param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c86b5-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86b5-117">包含與訊息相關聯之參數的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="c86b5-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86b5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="c86b5-118">Return value</span></span>

<span data-ttu-id="c86b5-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c86b5-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c86b5-120">備註</span><span class="sxs-lookup"><span data-stu-id="c86b5-120">Remarks</span></span>

<span data-ttu-id="c86b5-121">以非同步方式傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="c86b5-121">The message is sent asynchronously.</span></span> <span data-ttu-id="c86b5-122">也就是說，這個方法會立即傳回，而不是等候處理訊息。</span><span class="sxs-lookup"><span data-stu-id="c86b5-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="c86b5-123">當外掛程式完成處理訊息時，它會呼叫 [IWMPContentPartnerCallback：： SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) 方法，進而呼叫腳本的 [OnSendMessageComplete](external-onsendmessagecomplete-event.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c86b5-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86b5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c86b5-124">Requirements</span></span>



| <span data-ttu-id="c86b5-125">需求</span><span class="sxs-lookup"><span data-stu-id="c86b5-125">Requirement</span></span> | <span data-ttu-id="c86b5-126">值</span><span class="sxs-lookup"><span data-stu-id="c86b5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c86b5-127">版本</span><span class="sxs-lookup"><span data-stu-id="c86b5-127">Version</span></span><br/> | <span data-ttu-id="c86b5-128">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="c86b5-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c86b5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c86b5-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c86b5-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c86b5-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c86b5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c86b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86b5-132">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="c86b5-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c86b5-133">**OnSendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="c86b5-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="c86b5-134">**IWMPContentPartner：： SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c86b5-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="c86b5-135">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="c86b5-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





