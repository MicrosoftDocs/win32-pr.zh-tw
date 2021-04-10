---
description: Capture 篩選器的 Etype/SAP 部分會通知網路監視器驅動程式，接受具有特定 Etypes 和服務存取點組合的框架)  (Sap。
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: 撰寫 Etype/SAP 篩選部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944837"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="6e3a3-103">撰寫 Etype/SAP 篩選部分</span><span class="sxs-lookup"><span data-stu-id="6e3a3-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="6e3a3-104">Capture 篩選器的 Etype/SAP 部分會通知網路監視器驅動程式，接受具有特定 Etypes 和 [*服務存取點*](s.md) 組合的框架)  (sap。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="6e3a3-105">Etypes 和 Sap 是低層級的通訊協定（例如乙太網路、LLC 和貼齊）指出接下來的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="6e3a3-106">具體來說：</span><span class="sxs-lookup"><span data-stu-id="6e3a3-106">Specifically:</span></span>

-   <span data-ttu-id="6e3a3-107">Ethernet 指定 Etype</span><span class="sxs-lookup"><span data-stu-id="6e3a3-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="6e3a3-108">LLC 指定 SAP</span><span class="sxs-lookup"><span data-stu-id="6e3a3-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="6e3a3-109">貼齊會指定 Etype</span><span class="sxs-lookup"><span data-stu-id="6e3a3-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="6e3a3-110">Etype/SAP Capture 篩選旗標</span><span class="sxs-lookup"><span data-stu-id="6e3a3-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="6e3a3-111">您可以使用下列資訊，在 [**CAPTUREFILTER**](capturefilter.md)結構的 **FilterFlags** 成員中設定旗標。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="6e3a3-112">旗標</span><span class="sxs-lookup"><span data-stu-id="6e3a3-112">Flag</span></span>                                         | <span data-ttu-id="6e3a3-113">意義</span><span class="sxs-lookup"><span data-stu-id="6e3a3-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3a3-114">CAPTUREFILTER \_ 旗標 \_ 包括 \_ 所有 \_ SAP</span><span class="sxs-lookup"><span data-stu-id="6e3a3-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="6e3a3-115">傳遞所有 SAP 值，並通知驅動程式所有的 SAP 值都有效。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="6e3a3-116">如果與 **lpSapTable** 成員中的任何值結合，此旗標會通知驅動程式，除了 **lpSapTable** 中的所有 SAP 值都有效。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="6e3a3-117">CAPTUREFILTER \_ 旗標 \_ 包含 \_ 所有 \_ ETYPES</span><span class="sxs-lookup"><span data-stu-id="6e3a3-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="6e3a3-118">傳遞所有的 Etype 值，並通知驅動程式所有 Etype 值都有效。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="6e3a3-119">如果與 **lpEtypeTable** 成員中的任何值結合，此旗標會通知驅動程式，除了 **lpEtypeTable** 中的所有 Etype 值都有效。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="6e3a3-120">\_ \_ 僅限本機 CAPTUREFILTER 旗標 \_</span><span class="sxs-lookup"><span data-stu-id="6e3a3-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="6e3a3-121">設定此旗標不會將 NIC 設定為 P 模式。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="6e3a3-122">您只會看到本機電腦上 (任何畫面格) 的本機流量。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="6e3a3-123">CAPTUREFILTER \_ 旗標 \_ 保持 \_ RAW</span><span class="sxs-lookup"><span data-stu-id="6e3a3-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="6e3a3-124">保留 SMT 和權杖環形 MAC 框架。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="6e3a3-125">Etype/SAP Capture 篩選器設定</span><span class="sxs-lookup"><span data-stu-id="6e3a3-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="6e3a3-126">您可以使用下列資訊來設定 [**CAPTUREFILTER**](capturefilter.md)結構的 **lpSapTable** 和 **lpEtypeTable** 成員。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="6e3a3-127">設定</span><span class="sxs-lookup"><span data-stu-id="6e3a3-127">Setting</span></span>          | <span data-ttu-id="6e3a3-128">意義</span><span class="sxs-lookup"><span data-stu-id="6e3a3-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3a3-129">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-129">**lpSapTable**</span></span>   | <span data-ttu-id="6e3a3-130">列出您想要驅動程式傳遞的 SAP 值。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="6e3a3-131">這份清單會告知網路監視器驅動程式驗證封裝含相符項的任何框架。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="6e3a3-132">如果 \_ 已設定 CAPTUREFILTER 旗標 \_ 包括 \_ 所有 \_ sap，則會變成例外狀況清單 (如果找到的話，請不要傳遞) 。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="6e3a3-133">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-133">**lpEtypeTable**</span></span> | <span data-ttu-id="6e3a3-134">列出您想要網路監視器驅動程式傳遞的 Etype 值。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="6e3a3-135">這份清單只會告知驅動程式驗證封裝含相符的任何框架。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="6e3a3-136">如果 CAPTUREFILTER \_ 旗 \_ 標 \_ 包含 \_ 已設定的所有 ETYPES，這會變成例外狀況清單 (如果找到的話，請不要傳遞) 。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




