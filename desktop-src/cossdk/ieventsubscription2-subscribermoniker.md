---
description: 訂閱者的名字。
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: IEventSubscription2SubscriberMoniker 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688828"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="9fa33-103">IEventSubscription2：： SubscriberMoniker 屬性</span><span class="sxs-lookup"><span data-stu-id="9fa33-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="9fa33-104">訂閱者的名字。</span><span class="sxs-lookup"><span data-stu-id="9fa33-104">The subscriber's moniker.</span></span>

<span data-ttu-id="9fa33-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9fa33-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa33-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fa33-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="9fa33-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="9fa33-107">Property value</span></span>

<span data-ttu-id="9fa33-108">指定訂閱者的標記字串。</span><span class="sxs-lookup"><span data-stu-id="9fa33-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9fa33-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9fa33-109">Error codes</span></span>

<span data-ttu-id="9fa33-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9fa33-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa33-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fa33-111">Requirements</span></span>



| <span data-ttu-id="9fa33-112">需求</span><span class="sxs-lookup"><span data-stu-id="9fa33-112">Requirement</span></span> | <span data-ttu-id="9fa33-113">值</span><span class="sxs-lookup"><span data-stu-id="9fa33-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9fa33-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fa33-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa33-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fa33-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9fa33-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fa33-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa33-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fa33-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9fa33-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fa33-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa33-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="9fa33-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




