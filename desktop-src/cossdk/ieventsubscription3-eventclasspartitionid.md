---
description: 事件類別物件的資料分割 GUID。
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: IEventSubscription3：： EventClassPartitionID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510712"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="ef3e9-103">IEventSubscription3：： EventClassPartitionID 屬性</span><span class="sxs-lookup"><span data-stu-id="ef3e9-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="ef3e9-104">事件類別物件的資料分割 GUID。</span><span class="sxs-lookup"><span data-stu-id="ef3e9-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="ef3e9-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ef3e9-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3e9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef3e9-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="ef3e9-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="ef3e9-107">Property value</span></span>

<span data-ttu-id="ef3e9-108">字串，包含事件類別分割的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ef3e9-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef3e9-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ef3e9-109">Error codes</span></span>

<span data-ttu-id="ef3e9-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ef3e9-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef3e9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef3e9-111">Requirements</span></span>



| <span data-ttu-id="ef3e9-112">需求</span><span class="sxs-lookup"><span data-stu-id="ef3e9-112">Requirement</span></span> | <span data-ttu-id="ef3e9-113">值</span><span class="sxs-lookup"><span data-stu-id="ef3e9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ef3e9-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef3e9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3e9-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef3e9-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef3e9-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef3e9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3e9-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef3e9-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ef3e9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef3e9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3e9-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




