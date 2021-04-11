---
description: 確認資料存放區中的所有暫時性訂閱者是否存在。 藉由呼叫這個方法，您可以確保資料存放區中列出的所有暫時性訂閱者都在作用中。
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: IEventSystem2：： VerifyTransientSubscribers 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936228"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="6f4f5-104">IEventSystem2：： VerifyTransientSubscribers 方法</span><span class="sxs-lookup"><span data-stu-id="6f4f5-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="6f4f5-105">確認資料存放區中的所有暫時性訂閱者是否存在。</span><span class="sxs-lookup"><span data-stu-id="6f4f5-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="6f4f5-106">藉由呼叫這個方法，您可以確保資料存放區中列出的所有暫時性訂閱者都在作用中。</span><span class="sxs-lookup"><span data-stu-id="6f4f5-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4f5-107">語法</span><span class="sxs-lookup"><span data-stu-id="6f4f5-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="6f4f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="6f4f5-108">Parameters</span></span>

<span data-ttu-id="6f4f5-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6f4f5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f4f5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f4f5-110">Return value</span></span>

<span data-ttu-id="6f4f5-111">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6f4f5-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4f5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f4f5-112">Requirements</span></span>



| <span data-ttu-id="6f4f5-113">需求</span><span class="sxs-lookup"><span data-stu-id="6f4f5-113">Requirement</span></span> | <span data-ttu-id="6f4f5-114">值</span><span class="sxs-lookup"><span data-stu-id="6f4f5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6f4f5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f4f5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4f5-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f4f5-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f4f5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f4f5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4f5-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f4f5-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6f4f5-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f4f5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4f5-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="6f4f5-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




