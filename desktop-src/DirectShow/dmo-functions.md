---
description: SQL-DMO 函數
ms.assetid: 0a380dc0-23f0-4ef0-898a-3b5afddf5eaa
title: SQL-DMO 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f41750f5e442d93d3cacb2499bf2986a53cda6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467429"
---
# <a name="dmo-functions"></a><span data-ttu-id="97177-103">SQL-DMO 函數</span><span class="sxs-lookup"><span data-stu-id="97177-103">DMO Functions</span></span>

<span data-ttu-id="97177-104">本節說明 Microsoft DirectX Media 物件 (SQL-DMO) 函式。</span><span class="sxs-lookup"><span data-stu-id="97177-104">This section describes the Microsoft DirectX Media Object (DMO) functions.</span></span>



| <span data-ttu-id="97177-105">函式</span><span class="sxs-lookup"><span data-stu-id="97177-105">Function</span></span>                                             | <span data-ttu-id="97177-106">描述</span><span class="sxs-lookup"><span data-stu-id="97177-106">Description</span></span>                                                   |
|------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="97177-107">**DMOEnum**</span><span class="sxs-lookup"><span data-stu-id="97177-107">**DMOEnum**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)                           | <span data-ttu-id="97177-108">列舉登錄中所列的 DMOs。</span><span class="sxs-lookup"><span data-stu-id="97177-108">Enumerates DMOs listed in the registry.</span></span>                       |
| [<span data-ttu-id="97177-109">**DMOGetName**</span><span class="sxs-lookup"><span data-stu-id="97177-109">**DMOGetName**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogetname)                     | <span data-ttu-id="97177-110">從登錄抓取 SQL-DMO 的名稱。</span><span class="sxs-lookup"><span data-stu-id="97177-110">Retrieves the name of a DMO from the registry.</span></span>                |
| [<span data-ttu-id="97177-111">**DMOGetTypes**</span><span class="sxs-lookup"><span data-stu-id="97177-111">**DMOGetTypes**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogettypes)                   | <span data-ttu-id="97177-112">抓取註冊的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="97177-112">Retrieves the media types registered for a DMO.</span></span>               |
| [<span data-ttu-id="97177-113">**DMORegister**</span><span class="sxs-lookup"><span data-stu-id="97177-113">**DMORegister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister)                   | <span data-ttu-id="97177-114">註冊 a。</span><span class="sxs-lookup"><span data-stu-id="97177-114">Registers a DMO.</span></span>                                              |
| [<span data-ttu-id="97177-115">**DMOUnregister**</span><span class="sxs-lookup"><span data-stu-id="97177-115">**DMOUnregister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister)               | <span data-ttu-id="97177-116">取消註冊。</span><span class="sxs-lookup"><span data-stu-id="97177-116">Unregisters a DMO.</span></span>                                            |
| [<span data-ttu-id="97177-117">**MoCopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="97177-117">**MoCopyMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocopymediatype)           | <span data-ttu-id="97177-118">將一個媒體類型結構複製到另一個。</span><span class="sxs-lookup"><span data-stu-id="97177-118">Copies one media type structure to another.</span></span>                   |
| [<span data-ttu-id="97177-119">**MoCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="97177-119">**MoCreateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocreatemediatype)       | <span data-ttu-id="97177-120">配置新的媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="97177-120">Allocates a new media type structure.</span></span>                         |
| [<span data-ttu-id="97177-121">**MoDeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="97177-121">**MoDeleteMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-modeletemediatype)       | <span data-ttu-id="97177-122">刪除先前配置的媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="97177-122">Deletes a media type structure that was previously allocated.</span></span> |
| [<span data-ttu-id="97177-123">**MoDuplicateMediaType**</span><span class="sxs-lookup"><span data-stu-id="97177-123">**MoDuplicateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moduplicatemediatype) | <span data-ttu-id="97177-124">複製媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="97177-124">Duplicates a media type structure.</span></span>                            |
| [<span data-ttu-id="97177-125">**MoFreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="97177-125">**MoFreeMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mofreemediatype)           | <span data-ttu-id="97177-126">釋出媒體類型結構的配置成員。</span><span class="sxs-lookup"><span data-stu-id="97177-126">Frees the allocated members of a media type structure.</span></span>        |
| [<span data-ttu-id="97177-127">**MoInitMediaType**</span><span class="sxs-lookup"><span data-stu-id="97177-127">**MoInitMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moinitmediatype)           | <span data-ttu-id="97177-128">初始化媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="97177-128">Initializes a media type structure.</span></span>                           |



 

## <a name="related-topics"></a><span data-ttu-id="97177-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="97177-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97177-130">SQL-DMO 參考</span><span class="sxs-lookup"><span data-stu-id="97177-130">DMO Reference</span></span>](dmo-reference.md)
</dt> </dl>

 

 



