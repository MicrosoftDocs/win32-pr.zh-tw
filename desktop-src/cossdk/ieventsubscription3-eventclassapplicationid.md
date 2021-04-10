---
description: 事件類別物件的應用程式 GUID。
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: IEventSubscription3：： EventClassApplicationID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110913"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a><span data-ttu-id="2d7d8-103">IEventSubscription3：： EventClassApplicationID 屬性</span><span class="sxs-lookup"><span data-stu-id="2d7d8-103">IEventSubscription3::EventClassApplicationID property</span></span>

<span data-ttu-id="2d7d8-104">事件類別物件的應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="2d7d8-104">The application GUID of the event class object.</span></span>

<span data-ttu-id="2d7d8-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d7d8-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d7d8-106">Syntax</span></span>


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="2d7d8-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="2d7d8-107">Property value</span></span>

<span data-ttu-id="2d7d8-108">字串，包含事件類別應用程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2d7d8-108">A string containing the GUID of the event class application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d7d8-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2d7d8-109">Error codes</span></span>

<span data-ttu-id="2d7d8-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2d7d8-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d7d8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d7d8-111">Requirements</span></span>



| <span data-ttu-id="2d7d8-112">需求</span><span class="sxs-lookup"><span data-stu-id="2d7d8-112">Requirement</span></span> | <span data-ttu-id="2d7d8-113">值</span><span class="sxs-lookup"><span data-stu-id="2d7d8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2d7d8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d7d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2d7d8-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d7d8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2d7d8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d7d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2d7d8-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d7d8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2d7d8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d7d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7d8-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="2d7d8-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




