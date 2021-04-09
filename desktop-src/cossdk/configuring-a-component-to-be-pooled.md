---
description: 您可以設定只有在已正確寫入元件以支援進行共用時，才會將它設定為集區。 如需這些需求的詳細資訊，請參閱共用物件的需求。
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: 設定要共用的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111448"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="a0d10-104">設定要共用的元件</span><span class="sxs-lookup"><span data-stu-id="a0d10-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="a0d10-105">您可以設定只有在已正確寫入元件以支援進行共用時，才會將它設定為集區。</span><span class="sxs-lookup"><span data-stu-id="a0d10-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="a0d10-106">如需這些需求的詳細資訊，請參閱 [共用物件的需求](requirements-for-poolable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="a0d10-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0d10-107">依預設，元件不會設定為集區。</span><span class="sxs-lookup"><span data-stu-id="a0d10-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="a0d10-108">當您設定要共用的元件時，可以指定下列屬性來決定 COM + 如何維護集區：</span><span class="sxs-lookup"><span data-stu-id="a0d10-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="a0d10-109">**最小集區大小。**</span><span class="sxs-lookup"><span data-stu-id="a0d10-109">**Minimum pool size.**</span></span> <span data-ttu-id="a0d10-110">表示應用程式啟動時所建立的物件數目，以及在應用程式執行時，集區中維護的物件數目下限。</span><span class="sxs-lookup"><span data-stu-id="a0d10-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="a0d10-111">如果集區中可用的物件數目降到低於指定的最小值，就會建立新的物件來符合任何未處理的物件要求，並重新填滿集區。</span><span class="sxs-lookup"><span data-stu-id="a0d10-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="a0d10-112">如果集區中可用的物件數目大於最小數目，則會在清除週期期間終結這些剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="a0d10-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="a0d10-113">**最大集區大小。**</span><span class="sxs-lookup"><span data-stu-id="a0d10-113">**Maximum pool size.**</span></span> <span data-ttu-id="a0d10-114">代表共用管理員將建立的集區物件數目上限，同時由用戶端主動使用和集區中非使用中。</span><span class="sxs-lookup"><span data-stu-id="a0d10-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="a0d10-115">建立物件時，共用管理員會檢查以確認尚未達到集區大小上限，如果沒有，則集區管理員會建立要分配給用戶端之物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="a0d10-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="a0d10-116">如果已達到最大集區大小，用戶端要求將會排入佇列，並且會先以先服務的方式從集區接收第一個可用的物件。</span><span class="sxs-lookup"><span data-stu-id="a0d10-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="a0d10-117">物件建立要求會在指定的期間之後超時。</span><span class="sxs-lookup"><span data-stu-id="a0d10-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="a0d10-118">**建立 timeout (ms) 。**</span><span class="sxs-lookup"><span data-stu-id="a0d10-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="a0d10-119">指定在呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)之後，從集區傳回物件的用戶端會等待的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0d10-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="a0d10-120">如果用戶端呼叫失敗，則 \_ 會傳回錯誤 E TIMEOUT。</span><span class="sxs-lookup"><span data-stu-id="a0d10-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="a0d10-121">**若要設定共用相關屬性**</span><span class="sxs-lookup"><span data-stu-id="a0d10-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="a0d10-122">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="a0d10-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="a0d10-123">在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a0d10-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="a0d10-124">若要啟用元件的物件共用，請選取 [ **啟用物件** 共用] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="a0d10-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="a0d10-125">在 [ **最小集區大小** ] 方塊中，輸入此類型在集區中的最小物件數目。</span><span class="sxs-lookup"><span data-stu-id="a0d10-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="a0d10-126">集區將維持至少這個物件的數目。</span><span class="sxs-lookup"><span data-stu-id="a0d10-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="a0d10-127">在 [u] 方塊中，輸入此類型在集區中的最大物件數目。</span><span class="sxs-lookup"><span data-stu-id="a0d10-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="a0d10-128">物件數目（啟用和停用）永遠不會超過此值。</span><span class="sxs-lookup"><span data-stu-id="a0d10-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="a0d10-129">在 [ **建立超時 (ms)** ] 方塊中，輸入用戶端會等待集區物件的時間（以毫秒為單位）（如果無法立即使用的話）。</span><span class="sxs-lookup"><span data-stu-id="a0d10-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0d10-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0d10-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d10-131">監視物件統計資料</span><span class="sxs-lookup"><span data-stu-id="a0d10-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 
