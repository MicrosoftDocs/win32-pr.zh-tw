---
title: OnLoginChange 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnLoginChange 事件
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- External. OnLoginChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000669"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="305b7-105">OnLoginChange 事件</span><span class="sxs-lookup"><span data-stu-id="305b7-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="305b7-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="305b7-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="305b7-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="305b7-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="305b7-108">當使用者的登入狀態變更或登入嘗試失敗時，就會發生 **OnLoginChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="305b7-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="305b7-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="305b7-109">Possible Values</span></span>

<span data-ttu-id="305b7-110">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="305b7-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="305b7-111">參數</span><span class="sxs-lookup"><span data-stu-id="305b7-111">Parameters</span></span>

<span data-ttu-id="305b7-112">處理此事件的函式不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="305b7-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="305b7-113">備註</span><span class="sxs-lookup"><span data-stu-id="305b7-113">Remarks</span></span>

<span data-ttu-id="305b7-114">每次線上商店的外掛程式呼叫 [IWMPContentPartnerCallback：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)、在 *類型* 參數中傳遞 wmpcnLoginStateChange 時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="305b7-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="305b7-115">有時候外掛程式會進行此呼叫，以通知 Windows Media Player 使用者的登入狀態有所變更。</span><span class="sxs-lookup"><span data-stu-id="305b7-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="305b7-116">其他時候，外掛程式會進行此呼叫，以通知玩家登入嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="305b7-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="305b7-117">**Notify** 方法的 *pCoNtext* 參數會指定通知是要變更登入狀態，還是嘗試登入失敗。</span><span class="sxs-lookup"><span data-stu-id="305b7-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="305b7-118">由於每個呼叫 `Notify(wmpcnLoginStateChange, ...)` 都會導致 Windows Media Player 引發 **OnLoginChange** 事件，因此會呼叫 **OnLoginChange** 事件處理常式，有時是因為登入狀態變更的結果，有時也是因為登入嘗試失敗的結果。</span><span class="sxs-lookup"><span data-stu-id="305b7-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="305b7-119">若要判斷使用者目前的登入狀態， **OnLoginChange** 事件處理常式必須呼叫 [External. userLoggedIn](external-userloggedin.md)。</span><span class="sxs-lookup"><span data-stu-id="305b7-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="305b7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="305b7-120">Requirements</span></span>



| <span data-ttu-id="305b7-121">需求</span><span class="sxs-lookup"><span data-stu-id="305b7-121">Requirement</span></span> | <span data-ttu-id="305b7-122">值</span><span class="sxs-lookup"><span data-stu-id="305b7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="305b7-123">版本</span><span class="sxs-lookup"><span data-stu-id="305b7-123">Version</span></span><br/> | <span data-ttu-id="305b7-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="305b7-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="305b7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="305b7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="305b7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="305b7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="305b7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="305b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="305b7-128">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="305b7-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="305b7-129">**AttemptLogin**</span><span class="sxs-lookup"><span data-stu-id="305b7-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="305b7-130">**UserLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="305b7-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





