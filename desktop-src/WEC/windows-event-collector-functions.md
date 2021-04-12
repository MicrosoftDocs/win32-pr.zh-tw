---
title: Windows 事件收集器函式
description: 下列清單簡要說明 Windows 事件收集器中使用的函數。
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300028"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="9af2c-103">Windows 事件收集器函式</span><span class="sxs-lookup"><span data-stu-id="9af2c-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="9af2c-104">下列清單簡要說明 Windows 事件收集器中使用的函數。</span><span class="sxs-lookup"><span data-stu-id="9af2c-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9af2c-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="9af2c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9af2c-106">**EcClose**</span><span class="sxs-lookup"><span data-stu-id="9af2c-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="9af2c-107">關閉從其他事件收集器函數接收的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9af2c-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-108">**EcDeleteSubscription**</span><span class="sxs-lookup"><span data-stu-id="9af2c-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="9af2c-109">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9af2c-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-110">**EcEnumNextSubscription**</span><span class="sxs-lookup"><span data-stu-id="9af2c-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="9af2c-111">繼續列舉在本機電腦上註冊的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9af2c-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-112">**EcGetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="9af2c-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="9af2c-113">抓取訂用帳戶之事件來源的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9af2c-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-114">**EcGetObjectArraySize**</span><span class="sxs-lookup"><span data-stu-id="9af2c-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="9af2c-115">抓取訂用帳戶之事件來源的屬性值陣列的索引數目。</span><span class="sxs-lookup"><span data-stu-id="9af2c-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-116">**EcGetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="9af2c-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="9af2c-117">從訂用帳戶物件中抓取屬性值。</span><span class="sxs-lookup"><span data-stu-id="9af2c-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-118">**EcGetSubscriptionRunTimeStatus**</span><span class="sxs-lookup"><span data-stu-id="9af2c-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="9af2c-119">抓取訂用帳戶或訂用帳戶本身之事件來源的執行時間狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9af2c-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-120">**EcInsertObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="9af2c-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="9af2c-121">將空的物件插入至訂用帳戶之事件來源的屬性值陣列中。</span><span class="sxs-lookup"><span data-stu-id="9af2c-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-122">**EcOpenSubscriptionEnum**</span><span class="sxs-lookup"><span data-stu-id="9af2c-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="9af2c-123">建立訂閱列舉值，以列舉本機電腦上所有已註冊的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9af2c-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-124">**EcOpenSubscription**</span><span class="sxs-lookup"><span data-stu-id="9af2c-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="9af2c-125">開啟現有的訂用帳戶，或建立新的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="9af2c-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-126">**EcSaveSubscription**</span><span class="sxs-lookup"><span data-stu-id="9af2c-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="9af2c-127">儲存訂用帳戶設定資訊。</span><span class="sxs-lookup"><span data-stu-id="9af2c-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-128">**EcSetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="9af2c-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="9af2c-129">針對訂用帳戶的事件來源，設定屬性值陣列中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9af2c-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-130">**EcSetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="9af2c-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="9af2c-131">設定新值或更新訂用帳戶的現有值。</span><span class="sxs-lookup"><span data-stu-id="9af2c-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-132">**EcRemoveObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="9af2c-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="9af2c-133">從包含訂用帳戶之事件來源屬性值的物件陣列中移除元素。</span><span class="sxs-lookup"><span data-stu-id="9af2c-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="9af2c-134">**EcRetrySubscription**</span><span class="sxs-lookup"><span data-stu-id="9af2c-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="9af2c-135">重試連接到未連接之訂用帳戶的事件來源。</span><span class="sxs-lookup"><span data-stu-id="9af2c-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




