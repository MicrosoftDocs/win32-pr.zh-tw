---
title: Rich Edit 結構
description: Rich Edit 結構
ms.assetid: f7679e81-0a50-408b-8f60-9a3da4650f2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e63005040ca5b980f8aa78f7db8039b1e5254dd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853747"
---
# <a name="rich-edit-structures"></a><span data-ttu-id="5896b-103">Rich Edit 結構</span><span class="sxs-lookup"><span data-stu-id="5896b-103">Rich Edit Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5896b-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="5896b-104">In this section</span></span>

-   [<span data-ttu-id="5896b-105">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5896b-105">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
-   [<span data-ttu-id="5896b-106">**CHANGENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="5896b-106">**CHANGENOTIFY**</span></span>](/windows/desktop/api/Textserv/ns-textserv-changenotify)
-   [<span data-ttu-id="5896b-107">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5896b-107">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
-   [<span data-ttu-id="5896b-108">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="5896b-108">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
-   [<span data-ttu-id="5896b-109">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="5896b-109">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
-   [<span data-ttu-id="5896b-110">**CLIPBOARDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5896b-110">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
-   [<span data-ttu-id="5896b-111">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="5896b-111">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
-   [<span data-ttu-id="5896b-112">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="5896b-112">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
-   [<span data-ttu-id="5896b-113">**ENCORRECTTEXT**</span><span class="sxs-lookup"><span data-stu-id="5896b-113">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
-   [<span data-ttu-id="5896b-114">**ENDCOMPOSITIONNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="5896b-114">**ENDCOMPOSITIONNOTIFY**</span></span>](/windows/win32/api/richedit/ns-richedit-endcompositionnotify)
-   [<span data-ttu-id="5896b-115">**ENDROPFILES**</span><span class="sxs-lookup"><span data-stu-id="5896b-115">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
-   [<span data-ttu-id="5896b-116">**ENLINK**</span><span class="sxs-lookup"><span data-stu-id="5896b-116">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
-   [<span data-ttu-id="5896b-117">**ENLOWFIRTF**</span><span class="sxs-lookup"><span data-stu-id="5896b-117">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
-   [<span data-ttu-id="5896b-118">**ENOLEOPFAILED**</span><span class="sxs-lookup"><span data-stu-id="5896b-118">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
-   [<span data-ttu-id="5896b-119">**ENPROTECTED**</span><span class="sxs-lookup"><span data-stu-id="5896b-119">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
-   [<span data-ttu-id="5896b-120">**ENSAVECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="5896b-120">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
-   [<span data-ttu-id="5896b-121">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="5896b-121">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
-   [<span data-ttu-id="5896b-122">**FINDTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="5896b-122">**FINDTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-findtextexa)
-   [<span data-ttu-id="5896b-123">**FORMATRANGE**</span><span class="sxs-lookup"><span data-stu-id="5896b-123">**FORMATRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-formatrange)
-   [<span data-ttu-id="5896b-124">**GETCONTEXTMENUEX**</span><span class="sxs-lookup"><span data-stu-id="5896b-124">**GETCONTEXTMENUEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-getcontextmenuex)
-   [<span data-ttu-id="5896b-125">**GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="5896b-125">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
-   [<span data-ttu-id="5896b-126">**GETTEXTLENGTHEX**</span><span class="sxs-lookup"><span data-stu-id="5896b-126">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
-   [<span data-ttu-id="5896b-127">**HYPHENATEINFO**</span><span class="sxs-lookup"><span data-stu-id="5896b-127">**HYPHENATEINFO**</span></span>](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)
-   [<span data-ttu-id="5896b-128">**HYPHRESULT**</span><span class="sxs-lookup"><span data-stu-id="5896b-128">**HYPHRESULT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-hyphresult)
-   [<span data-ttu-id="5896b-129">**IMECOMPTEXT**</span><span class="sxs-lookup"><span data-stu-id="5896b-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
-   [<span data-ttu-id="5896b-130">**MSGFILTER**</span><span class="sxs-lookup"><span data-stu-id="5896b-130">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
-   [<span data-ttu-id="5896b-131">**OBJECTPOSITIONS**</span><span class="sxs-lookup"><span data-stu-id="5896b-131">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
-   [<span data-ttu-id="5896b-132">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5896b-132">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
-   [<span data-ttu-id="5896b-133">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="5896b-133">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
-   [<span data-ttu-id="5896b-134">**標點符號**</span><span class="sxs-lookup"><span data-stu-id="5896b-134">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
-   [<span data-ttu-id="5896b-135">**REOBJECT**</span><span class="sxs-lookup"><span data-stu-id="5896b-135">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
-   [<span data-ttu-id="5896b-136">**REPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="5896b-136">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
-   [<span data-ttu-id="5896b-137">**REQRESIZE**</span><span class="sxs-lookup"><span data-stu-id="5896b-137">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
-   [<span data-ttu-id="5896b-138">**RICHEDIT \_ 影像 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="5896b-138">**RICHEDIT\_IMAGE\_PARAMETERS**</span></span>](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters)
-   [<span data-ttu-id="5896b-139">**SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="5896b-139">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
-   [<span data-ttu-id="5896b-140">**SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="5896b-140">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
-   [<span data-ttu-id="5896b-141">**TABLECELLPARMS**</span><span class="sxs-lookup"><span data-stu-id="5896b-141">**TABLECELLPARMS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)
-   [<span data-ttu-id="5896b-142">**TABLEROWPARMS**</span><span class="sxs-lookup"><span data-stu-id="5896b-142">**TABLEROWPARMS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)
-   [<span data-ttu-id="5896b-143">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="5896b-143">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)

 

 




