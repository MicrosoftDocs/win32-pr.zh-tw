---
description: 訂閱者的資料分割 GUID。
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: IEventSubscription3：： SubscriberPartitionID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191028"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="0559d-103">IEventSubscription3：： SubscriberPartitionID 屬性</span><span class="sxs-lookup"><span data-stu-id="0559d-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="0559d-104">訂閱者的資料分割 GUID。</span><span class="sxs-lookup"><span data-stu-id="0559d-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="0559d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0559d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0559d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0559d-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="0559d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="0559d-107">Property value</span></span>

<span data-ttu-id="0559d-108">字串，其中包含訂閱者資料分割的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0559d-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0559d-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0559d-109">Error codes</span></span>

<span data-ttu-id="0559d-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0559d-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0559d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0559d-111">Requirements</span></span>



| <span data-ttu-id="0559d-112">需求</span><span class="sxs-lookup"><span data-stu-id="0559d-112">Requirement</span></span> | <span data-ttu-id="0559d-113">值</span><span class="sxs-lookup"><span data-stu-id="0559d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0559d-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0559d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0559d-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0559d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0559d-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0559d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0559d-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0559d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0559d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0559d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0559d-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="0559d-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




