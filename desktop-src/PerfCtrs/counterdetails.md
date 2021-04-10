---
description: CounterDetails 資料表描述特定電腦上的特定計數器。
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944266"
---
# <a name="counterdetails"></a><span data-ttu-id="010a9-103">CounterDetails</span><span class="sxs-lookup"><span data-stu-id="010a9-103">CounterDetails</span></span>

<span data-ttu-id="010a9-104">**CounterDetails** 資料表描述特定電腦上的特定計數器。</span><span class="sxs-lookup"><span data-stu-id="010a9-104">The **CounterDetails** table describes a specific counter on a particular computer.</span></span>

<span data-ttu-id="010a9-105">**CounterDetails** 資料表會定義下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="010a9-105">The **CounterDetails** table defines the following fields:</span></span>

-   <span data-ttu-id="010a9-106">**CounterID：** 資料庫中對應至特定計數器名稱文字字串的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="010a9-106">**CounterID:** A unique identifier in the database that maps to a specific counter name text string.</span></span> <span data-ttu-id="010a9-107">此欄位是此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="010a9-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="010a9-108">**MachineName：** 記錄此資料集的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="010a9-108">**MachineName:** The name of the computer that logged this data set.</span></span>
-   <span data-ttu-id="010a9-109">**ObjectName：** 效能物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="010a9-109">**ObjectName:** The name of the performance object.</span></span>
-   <span data-ttu-id="010a9-110">**CounterName：** 計數器的名稱。</span><span class="sxs-lookup"><span data-stu-id="010a9-110">**CounterName:** The name of the counter.</span></span>
-   <span data-ttu-id="010a9-111">**CounterType：** 計數器類型。</span><span class="sxs-lookup"><span data-stu-id="010a9-111">**CounterType:** The counter type.</span></span> <span data-ttu-id="010a9-112">如需計數器類型及其公式的清單，請參閱 [Windows Server 2003 部署套件](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10))的「計數器類型」一節。</span><span class="sxs-lookup"><span data-stu-id="010a9-112">For a list of counter types and their formulas, see the Counter Types section of the [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span></span>
-   <span data-ttu-id="010a9-113">**DefaultScale：** 要套用至原始效能計數器資料的預設調整。</span><span class="sxs-lookup"><span data-stu-id="010a9-113">**DefaultScale:** The default scaling to be applied to the raw performance counter data.</span></span>
-   <span data-ttu-id="010a9-114">**InstanceName：** 計數器實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="010a9-114">**InstanceName:** The name of the counter instance.</span></span>
-   <span data-ttu-id="010a9-115">**InstanceIndex：** 計數器實例的索引編號。</span><span class="sxs-lookup"><span data-stu-id="010a9-115">**InstanceIndex:** The index number of the counter instance.</span></span>
-   <span data-ttu-id="010a9-116">**ParentName：** 某些計數器會以邏輯方式與其他計數器相關聯，而且會被稱為父代。</span><span class="sxs-lookup"><span data-stu-id="010a9-116">**ParentName:** Some counters are logically associated with others, and are referred to as parents.</span></span> <span data-ttu-id="010a9-117">例如，執行緒的父系是一個進程，而邏輯磁片驅動程式的父系是實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="010a9-117">For example, the parent of a thread is a process and the parent of a logical disk driver is a physical drive.</span></span> <span data-ttu-id="010a9-118">此欄位包含父系的名稱。</span><span class="sxs-lookup"><span data-stu-id="010a9-118">This field contains the name of the parent.</span></span> <span data-ttu-id="010a9-119">這個欄位或 **父** 欄位中的值會識別特定的父實例。</span><span class="sxs-lookup"><span data-stu-id="010a9-119">Either the value in this field or the **ParentObjectID** field identifies a specific parent instance.</span></span> <span data-ttu-id="010a9-120">如果此欄位中的值為 **Null**，則必須核取 [ **父** ] 欄位中的值，以識別父代。</span><span class="sxs-lookup"><span data-stu-id="010a9-120">If the value in this field is **NULL**, the value in the **ParentObjectID** field must be checked to identify the parent.</span></span> <span data-ttu-id="010a9-121">如果兩個欄位中的值都是 **Null**，則計數器沒有父系。</span><span class="sxs-lookup"><span data-stu-id="010a9-121">If the values in both fields are **NULL**, the counter does not have a parent.</span></span>
-   <span data-ttu-id="010a9-122">**父：** 父系的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="010a9-122">**ParentObjectID:** The unique identifier of the parent.</span></span> <span data-ttu-id="010a9-123">這個欄位或 **ParentName** 欄位中的值會識別特定的父實例。</span><span class="sxs-lookup"><span data-stu-id="010a9-123">The value in either this field or the **ParentName** field identifies a specific parent instance.</span></span> <span data-ttu-id="010a9-124">如果此欄位中的值為 **Null**，則必須核取 [ **ParentName** ] 欄位中的值，以識別父代。</span><span class="sxs-lookup"><span data-stu-id="010a9-124">If the value in this field is **NULL**, the value in the **ParentName** field must be checked to identify the parent.</span></span>

 

 
