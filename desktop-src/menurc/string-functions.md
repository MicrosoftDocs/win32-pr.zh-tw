---
title: 字串函式
description: .
ms.assetid: 0249ea7a-84f1-4e25-9e80-0be5eb6c04ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b2f6c3f75e98de2f951f56aa2891eab72401a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372436"
---
# <a name="string-functions"></a><span data-ttu-id="2ad02-103">字串函式</span><span class="sxs-lookup"><span data-stu-id="2ad02-103">String Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ad02-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="2ad02-104">In This Section</span></span>

-   [<span data-ttu-id="2ad02-105">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="2ad02-105">**CharLower**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charlowera)
-   [<span data-ttu-id="2ad02-106">**CharLowerBuff**</span><span class="sxs-lookup"><span data-stu-id="2ad02-106">**CharLowerBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa)
-   [<span data-ttu-id="2ad02-107">**CharNext**</span><span class="sxs-lookup"><span data-stu-id="2ad02-107">**CharNext**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charnexta)
-   [<span data-ttu-id="2ad02-108">**CharNextExA**</span><span class="sxs-lookup"><span data-stu-id="2ad02-108">**CharNextExA**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charnextexa)
-   [<span data-ttu-id="2ad02-109">**CharPrev**</span><span class="sxs-lookup"><span data-stu-id="2ad02-109">**CharPrev**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charpreva)
-   [<span data-ttu-id="2ad02-110">**CharPrevExA**</span><span class="sxs-lookup"><span data-stu-id="2ad02-110">**CharPrevExA**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charprevexa)
-   [<span data-ttu-id="2ad02-111">**CharToOem**</span><span class="sxs-lookup"><span data-stu-id="2ad02-111">**CharToOem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-chartooema)
-   [<span data-ttu-id="2ad02-112">**CharToOemBuff**</span><span class="sxs-lookup"><span data-stu-id="2ad02-112">**CharToOemBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-chartooembuffa)
-   [<span data-ttu-id="2ad02-113">**CharUpper**</span><span class="sxs-lookup"><span data-stu-id="2ad02-113">**CharUpper**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charuppera)
-   [<span data-ttu-id="2ad02-114">**CharUpperBuff**</span><span class="sxs-lookup"><span data-stu-id="2ad02-114">**CharUpperBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa)
-   [<span data-ttu-id="2ad02-115">**IsCharAlpha**</span><span class="sxs-lookup"><span data-stu-id="2ad02-115">**IsCharAlpha**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)
-   [<span data-ttu-id="2ad02-116">**IsCharAlphaNumeric**</span><span class="sxs-lookup"><span data-stu-id="2ad02-116">**IsCharAlphaNumeric**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica)
-   [<span data-ttu-id="2ad02-117">**IsCharLower**</span><span class="sxs-lookup"><span data-stu-id="2ad02-117">**IsCharLower**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)
-   [<span data-ttu-id="2ad02-118">**IsCharUpper**</span><span class="sxs-lookup"><span data-stu-id="2ad02-118">**IsCharUpper**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)
-   [<span data-ttu-id="2ad02-119">**Loadstring 時**</span><span class="sxs-lookup"><span data-stu-id="2ad02-119">**LoadString**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadstringa)
-   [<span data-ttu-id="2ad02-120">**lstrcat**</span><span class="sxs-lookup"><span data-stu-id="2ad02-120">**lstrcat**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcata)
-   [<span data-ttu-id="2ad02-121">**lstrcmp**</span><span class="sxs-lookup"><span data-stu-id="2ad02-121">**lstrcmp**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa)
-   [<span data-ttu-id="2ad02-122">**lstrcmpi**</span><span class="sxs-lookup"><span data-stu-id="2ad02-122">**lstrcmpi**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcmpia)
-   [<span data-ttu-id="2ad02-123">**lstrcpy**</span><span class="sxs-lookup"><span data-stu-id="2ad02-123">**lstrcpy**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)
-   [<span data-ttu-id="2ad02-124">**lstrcpyn**</span><span class="sxs-lookup"><span data-stu-id="2ad02-124">**lstrcpyn**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcpyna)
-   [<span data-ttu-id="2ad02-125">**lstrlen**</span><span class="sxs-lookup"><span data-stu-id="2ad02-125">**lstrlen**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrlena)
-   [<span data-ttu-id="2ad02-126">**OemToChar**</span><span class="sxs-lookup"><span data-stu-id="2ad02-126">**OemToChar**</span></span>](/windows/desktop/api/Winuser/nf-winuser-oemtochara)
-   [<span data-ttu-id="2ad02-127">**OemToCharBuff**</span><span class="sxs-lookup"><span data-stu-id="2ad02-127">**OemToCharBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa)
-   [<span data-ttu-id="2ad02-128">**wsprintf**</span><span class="sxs-lookup"><span data-stu-id="2ad02-128">**wsprintf**</span></span>](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)
-   [<span data-ttu-id="2ad02-129">**wvsprintf**</span><span class="sxs-lookup"><span data-stu-id="2ad02-129">**wvsprintf**</span></span>](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)

 

 




