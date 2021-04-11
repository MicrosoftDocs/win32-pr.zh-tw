---
description: 管理訂用帳戶的篩選準則。
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: IEventSubscription2：： >filtercriteria 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111292"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="02a80-103">IEventSubscription2：： >filtercriteria 屬性</span><span class="sxs-lookup"><span data-stu-id="02a80-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="02a80-104">管理訂用帳戶的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="02a80-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="02a80-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="02a80-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a80-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a80-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="02a80-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="02a80-107">Property value</span></span>

<span data-ttu-id="02a80-108">執行 [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter)之類別的篩選準則或 CLSID。</span><span class="sxs-lookup"><span data-stu-id="02a80-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="02a80-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="02a80-109">Error codes</span></span>

<span data-ttu-id="02a80-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="02a80-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a80-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a80-111">Requirements</span></span>



| <span data-ttu-id="02a80-112">需求</span><span class="sxs-lookup"><span data-stu-id="02a80-112">Requirement</span></span> | <span data-ttu-id="02a80-113">值</span><span class="sxs-lookup"><span data-stu-id="02a80-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="02a80-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02a80-114">Minimum supported client</span></span><br/> | <span data-ttu-id="02a80-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02a80-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02a80-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02a80-116">Minimum supported server</span></span><br/> | <span data-ttu-id="02a80-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02a80-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="02a80-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a80-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a80-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="02a80-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




