---
description: 訂閱者的應用程式 GUID。
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: IEventSubscription3：： SubscriberApplicationID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187688"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="f4522-103">IEventSubscription3：： SubscriberApplicationID 屬性</span><span class="sxs-lookup"><span data-stu-id="f4522-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="f4522-104">訂閱者的應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="f4522-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="f4522-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4522-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4522-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4522-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="f4522-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f4522-107">Property value</span></span>

<span data-ttu-id="f4522-108">字串，其中包含訂閱者應用程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f4522-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4522-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f4522-109">Error codes</span></span>

<span data-ttu-id="f4522-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f4522-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4522-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4522-111">Requirements</span></span>



| <span data-ttu-id="f4522-112">需求</span><span class="sxs-lookup"><span data-stu-id="f4522-112">Requirement</span></span> | <span data-ttu-id="f4522-113">值</span><span class="sxs-lookup"><span data-stu-id="f4522-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f4522-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4522-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f4522-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4522-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f4522-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4522-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f4522-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4522-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f4522-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4522-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4522-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="f4522-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




