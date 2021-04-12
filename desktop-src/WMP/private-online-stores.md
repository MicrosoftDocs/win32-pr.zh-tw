---
title: 私人線上商店
description: 私人線上商店
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player 線上商店，私用
- 線上商店，私用
- 輸入1個線上商店，私用
- 輸入2個線上商店，私用
- 私人線上商店
- 登錄，私人線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372377"
---
# <a name="private-online-stores"></a><span data-ttu-id="39c6d-109">私人線上商店</span><span class="sxs-lookup"><span data-stu-id="39c6d-109">Private Online Stores</span></span>

<span data-ttu-id="39c6d-110">Windows Media Player 10 或更新版本支援私人線上商店;也就是說，只有特定使用者才會看到存放區。</span><span class="sxs-lookup"><span data-stu-id="39c6d-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="39c6d-111">若要讓目前的使用者看見私人線上商店，您必須在下列登錄機碼底下輸入代表私人線上商店的專案。</span><span class="sxs-lookup"><span data-stu-id="39c6d-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="39c6d-112">HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ PrivateServices</span><span class="sxs-lookup"><span data-stu-id="39c6d-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="39c6d-113">必要的登錄專案必須具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="39c6d-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="39c6d-114">名稱</span><span class="sxs-lookup"><span data-stu-id="39c6d-114">Name</span></span>                                                         | <span data-ttu-id="39c6d-115">類型</span><span class="sxs-lookup"><span data-stu-id="39c6d-115">Type</span></span>           | <span data-ttu-id="39c6d-116">值</span><span class="sxs-lookup"><span data-stu-id="39c6d-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="39c6d-117">建立登錄專案的人員所選擇的任何名稱</span><span class="sxs-lookup"><span data-stu-id="39c6d-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="39c6d-118">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="39c6d-118">**REG\_DWORD**</span></span> | <span data-ttu-id="39c6d-119">由 Microsoft 提供的數位，可識別私人線上商店</span><span class="sxs-lookup"><span data-stu-id="39c6d-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="39c6d-120">只有當控制項在遠端模式中執行時，Windows Media Player 10 ActiveX 控制項才支援私用線上存放區。</span><span class="sxs-lookup"><span data-stu-id="39c6d-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="39c6d-121">無論控制項是否以遠端模式執行，Windows Media Player 11 ActiveX 控制項都支援私用線上存放區。</span><span class="sxs-lookup"><span data-stu-id="39c6d-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39c6d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="39c6d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39c6d-123">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="39c6d-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




