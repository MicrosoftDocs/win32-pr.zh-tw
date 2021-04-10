---
description: CBasePin 連接進程
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: CBasePin 連接進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935799"
---
# <a name="cbasepin-connection-process"></a><span data-ttu-id="6c80f-103">CBasePin 連接進程</span><span class="sxs-lookup"><span data-stu-id="6c80f-103">CBasePin Connection Process</span></span>

<span data-ttu-id="6c80f-104">本節說明 [**CBasePin**](cbasepin.md) 類別如何執行 pin 連接程式。</span><span class="sxs-lookup"><span data-stu-id="6c80f-104">This section describes how the [**CBasePin**](cbasepin.md) class implements the pin connection process.</span></span>

<span data-ttu-id="6c80f-105">篩選圖形管理員會起始所有的釘選連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-105">The Filter Graph Manager initiates all pin connections.</span></span> <span data-ttu-id="6c80f-106">它會呼叫輸出釘選的 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法，並指定輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="6c80f-106">It calls the output pin's [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, specifying the input pin.</span></span> <span data-ttu-id="6c80f-107">輸出 pin 會藉由呼叫輸入釘選的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法來完成連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-107">The output pin completes the connection by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="6c80f-108">輸入 pin 可以接受或拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-108">The input pin can accept or reject the connection.</span></span>

<span data-ttu-id="6c80f-109">篩選圖形管理員也可以指定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6c80f-109">The Filter Graph Manager can also specify a media type for the connection.</span></span> <span data-ttu-id="6c80f-110">如果是，則會嘗試使用該類型連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-110">If so, the pins try to connect with that type.</span></span> <span data-ttu-id="6c80f-111">如果沒有，則 pin 必須協商型別。</span><span class="sxs-lookup"><span data-stu-id="6c80f-111">If not, the pins must negotiate the type.</span></span> <span data-ttu-id="6c80f-112">篩選圖形管理員也可以指定 *部分* 媒體類型，此類型的 \_ 主要類型、子類型或格式類型的值為 GUID Null。</span><span class="sxs-lookup"><span data-stu-id="6c80f-112">The Filter Graph Manager may also specify a *partial* media type, which has the value GUID\_NULL for either the major type, subtype, or format type.</span></span> <span data-ttu-id="6c80f-113">在這種情況下，pin 會嘗試比對媒體類型的任何部分（若已指定）;值 GUID \_ Null 可作為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="6c80f-113">In that case, the pins try to match whichever portions of the media type were specified; the value GUID\_NULL acts as a wildcard.</span></span>

<span data-ttu-id="6c80f-114">[**CBasePin：： Connect**](cbasepin-connect.md)方法一開始先確認 pin 可以接受連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-114">The [**CBasePin::Connect**](cbasepin-connect.md) method starts by verifying that the pin can accept a connection.</span></span> <span data-ttu-id="6c80f-115">例如，它會檢查 pin 是否尚未連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-115">For example, it checks that the pin is not already connected.</span></span> <span data-ttu-id="6c80f-116">它會將連接進程的其餘部分委派給 [**CBasePin：： AgreeMediaType**](cbasepin-agreemediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6c80f-116">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span> <span data-ttu-id="6c80f-117">接下來的所有專案都是由 **AgreeMediaType** 執行。</span><span class="sxs-lookup"><span data-stu-id="6c80f-117">Everything that follows is performed by **AgreeMediaType**.</span></span>

<span data-ttu-id="6c80f-118">如果媒體類型是完全指定的，則 pin 會呼叫 [**CBasePin：： AttemptConnection**](cbasepin-attemptconnection.md) 方法來嘗試連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-118">If the media type is fully specified, the pin calls the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method to attempt the connection.</span></span> <span data-ttu-id="6c80f-119">否則，它會依下列順序嘗試媒體類型：</span><span class="sxs-lookup"><span data-stu-id="6c80f-119">Otherwise, it tries media types in the following order:</span></span>

1.  <span data-ttu-id="6c80f-120">輸入釘選的慣用類型。</span><span class="sxs-lookup"><span data-stu-id="6c80f-120">The input pin's preferred types.</span></span>
2.  <span data-ttu-id="6c80f-121">輸出釘選的慣用類型。</span><span class="sxs-lookup"><span data-stu-id="6c80f-121">The output pin's preferred types.</span></span>

<span data-ttu-id="6c80f-122">您可以將 [**CBasePin：： m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) 旗標設為 **TRUE**，以反轉此順序。</span><span class="sxs-lookup"><span data-stu-id="6c80f-122">You can reverse this order by setting the [**CBasePin::m\_bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) flag to **TRUE**.</span></span>

<span data-ttu-id="6c80f-123">在每個案例中，pin 都會呼叫 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 來列舉媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6c80f-123">In each case, the pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) to enumerate the media types.</span></span> <span data-ttu-id="6c80f-124">這個方法會取出傳遞給 [**CBasePin：： TryMediaTypes**](cbasepin-trymediatypes.md) 方法的枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="6c80f-124">This method retrieves an enumerator object, which is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span> <span data-ttu-id="6c80f-125">**TryMediaTypes** 方法會在每個媒體類型之間執行迴圈，並針對每個類型呼叫 [**AttemptConnection**](cbasepin-attemptconnection.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c80f-125">The **TryMediaTypes** method loops through each media type and calls [**AttemptConnection**](cbasepin-attemptconnection.md) for each type.</span></span>

<span data-ttu-id="6c80f-126">在 [**AttemptConnection**](cbasepin-attemptconnection.md) 方法中，輸出圖釘會呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="6c80f-126">Within the [**AttemptConnection**](cbasepin-attemptconnection.md) method, the output pin calls the following methods:</span></span>

-   <span data-ttu-id="6c80f-127">它會自行呼叫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) ，以檢查輸入的 pin 是否適合。</span><span class="sxs-lookup"><span data-stu-id="6c80f-127">It calls [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) on itself, to check whether the input pin is suitable.</span></span>
-   <span data-ttu-id="6c80f-128">它本身會呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) ，以驗證媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6c80f-128">It calls [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) on itself, to validate the media type.</span></span>
-   <span data-ttu-id="6c80f-129">它會在輸入 pin 上呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 。</span><span class="sxs-lookup"><span data-stu-id="6c80f-129">It calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the input pin.</span></span> <span data-ttu-id="6c80f-130">輸入 pin 會使用這個方法來判斷是否應接受連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-130">The input pin uses this method to determine whether it should accept the connection.</span></span>
-   <span data-ttu-id="6c80f-131">它會自行呼叫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 來完成連接。</span><span class="sxs-lookup"><span data-stu-id="6c80f-131">It calls [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) on itself to completes the connection.</span></span>

<span data-ttu-id="6c80f-132">請注意：</span><span class="sxs-lookup"><span data-stu-id="6c80f-132">Note the following:</span></span>

-   <span data-ttu-id="6c80f-133">[**CheckConnect**](cbasepin-checkconnect.md) 是虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="6c80f-133">[**CheckConnect**](cbasepin-checkconnect.md) is a virtual method.</span></span> <span data-ttu-id="6c80f-134">在基類中，此方法會檢查釘選方向是否相容。</span><span class="sxs-lookup"><span data-stu-id="6c80f-134">In the base class, this method checks whether the pin directions are compatible.</span></span> <span data-ttu-id="6c80f-135">輸出 pin 必須連接到輸入圖釘，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="6c80f-135">Output pins must connect to input pins, and vice versa.</span></span> <span data-ttu-id="6c80f-136">衍生的 pin 類別通常會覆寫這個方法，以執行其他檢查。</span><span class="sxs-lookup"><span data-stu-id="6c80f-136">The derived pin class will typically override this method to perform other checks.</span></span> <span data-ttu-id="6c80f-137">例如，它可能會查詢連接所需介面的其他 pin。</span><span class="sxs-lookup"><span data-stu-id="6c80f-137">For example, it might query the other pin for an interface that is required for the connection.</span></span> <span data-ttu-id="6c80f-138">如果衍生類別覆寫 **CheckConnect**，則也應該呼叫 [**CBasePin**](cbasepin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6c80f-138">If the derived class overrides **CheckConnect**, it should also call the [**CBasePin**](cbasepin.md) method.</span></span>
-   <span data-ttu-id="6c80f-139">[**CheckMediaType**](cbasepin-checkmediatype.md) 是一種單純的虛擬方法，衍生類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="6c80f-139">[**CheckMediaType**](cbasepin-checkmediatype.md) is a pure virtual method, which the derived class must implement.</span></span>
-   <span data-ttu-id="6c80f-140">[**CompleteConnect**](cbasepin-completeconnect.md) 是不會在基類中執行任何動作的虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="6c80f-140">[**CompleteConnect**](cbasepin-completeconnect.md) is a virtual method that does nothing in the base class.</span></span> <span data-ttu-id="6c80f-141">衍生類別可以覆寫這個方法，以執行完成連接所需的任何其他工作，例如決定記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="6c80f-141">Derived classes can override this method to perform any additional work needed to complete the connection, such as deciding a memory allocator.</span></span>

<span data-ttu-id="6c80f-142">如果這些步驟中有任何一項失敗，輸出圖釘會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法，以復原 [**CheckConnect**](cbasepin-checkconnect.md)所採取的任何步驟。</span><span class="sxs-lookup"><span data-stu-id="6c80f-142">If any of these steps fails, the output pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to undo whatever steps were taken by [**CheckConnect**](cbasepin-checkconnect.md).</span></span>

<span data-ttu-id="6c80f-143">輸入釘選的 [**ReceiveConnection**](cbasepin-receiveconnection.md) 方法會呼叫輸入釘選的 [**CheckConnect**](cbasepin-checkconnect.md)、 [**CheckMediaType**](cbasepin-checkmediatype.md)和 [**CompleteConnect**](cbasepin-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6c80f-143">The input pin's [**ReceiveConnection**](cbasepin-receiveconnection.md) method calls the input pin's [**CheckConnect**](cbasepin-checkconnect.md), [**CheckMediaType**](cbasepin-checkmediatype.md), and [**CompleteConnect**](cbasepin-completeconnect.md) methods.</span></span> <span data-ttu-id="6c80f-144">如果其中任何一項失敗，連接嘗試也會失敗。</span><span class="sxs-lookup"><span data-stu-id="6c80f-144">If any of these fail, the connection attempt also fails.</span></span>

<span data-ttu-id="6c80f-145">下圖顯示 [**CBasePin**](cbasepin.md)中的連接程式：</span><span class="sxs-lookup"><span data-stu-id="6c80f-145">The following diagram shows the connection process in [**CBasePin**](cbasepin.md):</span></span>

![cbasepin 連接進程](images/cbasepin-connect.png)

## <a name="related-topics"></a><span data-ttu-id="6c80f-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c80f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c80f-148">**CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6c80f-148">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 



