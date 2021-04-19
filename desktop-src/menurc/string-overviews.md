---
title: '>strsafe.h 函式'
description: .
ms.assetid: 3590dd8d-3a88-4dde-a5fe-f10e12354919
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b31824788b68a7ec789c6d274b2a368eda1cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "107001078"
---
# <a name="strsafe-functions"></a><span data-ttu-id="6d210-103">>strsafe.h 函式</span><span class="sxs-lookup"><span data-stu-id="6d210-103">Strsafe Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6d210-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="6d210-104">In this section</span></span>

-   [<span data-ttu-id="6d210-105">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="6d210-105">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)
-   [<span data-ttu-id="6d210-106">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-106">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)
-   [<span data-ttu-id="6d210-107">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="6d210-107">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)
-   [<span data-ttu-id="6d210-108">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-108">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)
-   [<span data-ttu-id="6d210-109">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="6d210-109">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)
-   [<span data-ttu-id="6d210-110">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-110">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)
-   [<span data-ttu-id="6d210-111">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="6d210-111">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)
-   [<span data-ttu-id="6d210-112">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-112">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)
-   [<span data-ttu-id="6d210-113">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="6d210-113">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)
-   [<span data-ttu-id="6d210-114">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-114">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)
-   [<span data-ttu-id="6d210-115">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="6d210-115">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)
-   [<span data-ttu-id="6d210-116">**StringCbPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="6d210-116">**StringCbPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_la)
-   [<span data-ttu-id="6d210-117">**StringCbPrintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-117">**StringCbPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_lexa)
-   [<span data-ttu-id="6d210-118">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="6d210-118">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)
-   [<span data-ttu-id="6d210-119">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-119">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)
-   [<span data-ttu-id="6d210-120">**StringCbVPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="6d210-120">**StringCbVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_la)
-   [<span data-ttu-id="6d210-121">**StringCbVPrintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-121">**StringCbVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_lexa)
-   [<span data-ttu-id="6d210-122">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="6d210-122">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)
-   [<span data-ttu-id="6d210-123">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-123">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)
-   [<span data-ttu-id="6d210-124">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="6d210-124">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)
-   [<span data-ttu-id="6d210-125">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-125">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)
-   [<span data-ttu-id="6d210-126">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="6d210-126">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)
-   [<span data-ttu-id="6d210-127">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-127">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)
-   [<span data-ttu-id="6d210-128">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="6d210-128">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)
-   [<span data-ttu-id="6d210-129">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-129">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)
-   [<span data-ttu-id="6d210-130">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="6d210-130">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)
-   [<span data-ttu-id="6d210-131">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-131">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)
-   [<span data-ttu-id="6d210-132">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="6d210-132">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)
-   [<span data-ttu-id="6d210-133">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-133">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)
-   [<span data-ttu-id="6d210-134">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="6d210-134">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)
-   [<span data-ttu-id="6d210-135">**StringCchPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="6d210-135">**StringCchPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_la)
-   [<span data-ttu-id="6d210-136">**StringCchPrintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-136">**StringCchPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_lexa)
-   [<span data-ttu-id="6d210-137">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="6d210-137">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)
-   [<span data-ttu-id="6d210-138">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-138">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)
-   [<span data-ttu-id="6d210-139">**StringCchVPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="6d210-139">**StringCchVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_la)
-   [<span data-ttu-id="6d210-140">**StringCchVPrintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-140">**StringCchVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_lexa)
-   [<span data-ttu-id="6d210-141">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="6d210-141">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)
-   [<span data-ttu-id="6d210-142">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="6d210-142">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)
-   <span data-ttu-id="6d210-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d210-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span></span>
-   <span data-ttu-id="6d210-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d210-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span></span>

 

 