---
title: OnSendMessageComplete 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnSendMessageComplete 事件
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- External. OnSendMessageComplete 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977399"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="17437-105">OnSendMessageComplete 事件</span><span class="sxs-lookup"><span data-stu-id="17437-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="17437-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="17437-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="17437-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="17437-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="17437-108">當線上商店完成處理訊息時，就會發生 **OnSendMessageComplete** 事件。</span><span class="sxs-lookup"><span data-stu-id="17437-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="17437-109">探索頁面上的腳本先前藉由呼叫 [External. sendMessage](external-sendmessage.md)傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="17437-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="17437-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="17437-110">Possible Values</span></span>

<span data-ttu-id="17437-111">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="17437-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="17437-112">參數</span><span class="sxs-lookup"><span data-stu-id="17437-112">Parameters</span></span>

<span data-ttu-id="17437-113">處理此事件的函式具有下列參數。</span><span class="sxs-lookup"><span data-stu-id="17437-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="17437-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*味精*</span><span class="sxs-lookup"><span data-stu-id="17437-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="17437-115">在 **sendMessage** 的 **Msg** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="17437-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="17437-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*參數*</span><span class="sxs-lookup"><span data-stu-id="17437-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="17437-117">在 **sendMessage** 的 **Param** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="17437-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="17437-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*結果*</span><span class="sxs-lookup"><span data-stu-id="17437-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="17437-119">包含訊息處理結果的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="17437-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="17437-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="17437-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17437-121">備註</span><span class="sxs-lookup"><span data-stu-id="17437-121">Remarks</span></span>

<span data-ttu-id="17437-122">**SendMessage** 方法會呼叫 [IWMPContentPartner：： sendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)，它會以非同步方式傳回。</span><span class="sxs-lookup"><span data-stu-id="17437-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="17437-123">也就是說，它會在線上商店完成處理訊息之前傳回。</span><span class="sxs-lookup"><span data-stu-id="17437-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="17437-124">當線上商店完成處理訊息時，它會呼叫 [IWMPContentPartnerCallback：： SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)，進而呼叫腳本的 **OnSendMessageComplete** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="17437-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="17437-125">當線上商店呼叫 **IWMPContentPartnerCallback：： SendMessageComplete** 時，它會在 *bstrResult* 參數中提供結果碼。</span><span class="sxs-lookup"><span data-stu-id="17437-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="17437-126">Windows Media Player 不會解讀結果碼。</span><span class="sxs-lookup"><span data-stu-id="17437-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="17437-127">相反地，Windows Media Player 會將結果碼傳遞給 *result* 參數中的 **OnSendMessageComplete** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="17437-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="17437-128">**OnSendMessageComplete** 事件處理常式的 (*Msg*、 *Param*、 *Result*) 的參數都不是由 Windows Media Player 所解讀。</span><span class="sxs-lookup"><span data-stu-id="17437-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="17437-129">參數只有線上商店才有意義。</span><span class="sxs-lookup"><span data-stu-id="17437-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="17437-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="17437-130">Requirements</span></span>



| <span data-ttu-id="17437-131">需求</span><span class="sxs-lookup"><span data-stu-id="17437-131">Requirement</span></span> | <span data-ttu-id="17437-132">值</span><span class="sxs-lookup"><span data-stu-id="17437-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17437-133">版本</span><span class="sxs-lookup"><span data-stu-id="17437-133">Version</span></span><br/> | <span data-ttu-id="17437-134">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="17437-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="17437-135">DLL</span><span class="sxs-lookup"><span data-stu-id="17437-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="17437-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17437-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17437-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17437-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17437-138">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="17437-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="17437-139">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="17437-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="17437-140">**IWMPContentPartner：： SendMessage**</span><span class="sxs-lookup"><span data-stu-id="17437-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="17437-141">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="17437-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





