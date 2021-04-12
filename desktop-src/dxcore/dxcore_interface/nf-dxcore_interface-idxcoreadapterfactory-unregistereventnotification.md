---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: 從您先前註冊的通知中取消註冊。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376297"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="de9c6-103">IDXCoreAdapterFactory：： UnregisterEventNotification 方法</span><span class="sxs-lookup"><span data-stu-id="de9c6-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="de9c6-104">從您先前註冊的通知中取消註冊。</span><span class="sxs-lookup"><span data-stu-id="de9c6-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="de9c6-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="de9c6-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="de9c6-106">語法</span><span class="sxs-lookup"><span data-stu-id="de9c6-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="de9c6-107">參數</span><span class="sxs-lookup"><span data-stu-id="de9c6-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="de9c6-108">eventCookie</span><span class="sxs-lookup"><span data-stu-id="de9c6-108">eventCookie</span></span>

<span data-ttu-id="de9c6-109">類型： **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="de9c6-109">Type: **uint32_t**</span></span>

<span data-ttu-id="de9c6-110">當您呼叫 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) 代表您現在想要取消註冊的先前註冊時，會傳回 cookie 值 (傳回。</span><span class="sxs-lookup"><span data-stu-id="de9c6-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="de9c6-111">傳回</span><span class="sxs-lookup"><span data-stu-id="de9c6-111">Returns</span></span>

<span data-ttu-id="de9c6-112">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="de9c6-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="de9c6-113">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="de9c6-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="de9c6-114">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="de9c6-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="de9c6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="de9c6-115">Return value</span></span>|<span data-ttu-id="de9c6-116">描述</span><span class="sxs-lookup"><span data-stu-id="de9c6-116">Description</span></span>|
|-|-|
|<span data-ttu-id="de9c6-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="de9c6-117">E_INVALIDARG</span></span>|<span data-ttu-id="de9c6-118">*EventCookie* 的值不是代表先前註冊的有效 cookie。</span><span class="sxs-lookup"><span data-stu-id="de9c6-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="de9c6-119">備註</span><span class="sxs-lookup"><span data-stu-id="de9c6-119">Remarks</span></span>

<span data-ttu-id="de9c6-120">只有在此註冊的所有擱置/進行中的回呼都已完成之後， **UnregisterEventNotification** 才會傳回。</span><span class="sxs-lookup"><span data-stu-id="de9c6-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="de9c6-121">DXCore 保證在 **UnregisterEventNotification** 傳回之後，不會對此註冊進行新的回呼。</span><span class="sxs-lookup"><span data-stu-id="de9c6-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="de9c6-122">不過，若要避免鎖死，如果您從回呼內呼叫 **UnregisterEventNotification** ， **UnregisterEventNotification** 就不會等待作用中的回呼完成。</span><span class="sxs-lookup"><span data-stu-id="de9c6-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de9c6-123">在您終結傳遞給 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)之 *dxCoreObject* 引數所代表的 DXCore 物件之前，您必須使用 cookie 值，藉由呼叫 **UnregisterEventNotification** 從通知取消註冊該物件。</span><span class="sxs-lookup"><span data-stu-id="de9c6-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="de9c6-124">如果您沒有這麼做，則在偵測到情況時，就會引發嚴重的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="de9c6-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="de9c6-125">當您取消註冊 cookie 值之後，該值就會符合後續註冊所傳回的資格</span><span class="sxs-lookup"><span data-stu-id="de9c6-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="de9c6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de9c6-126">See also</span></span>

<span data-ttu-id="de9c6-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="de9c6-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>