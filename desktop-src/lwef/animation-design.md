---
title: 動畫設計
description: 動畫設計
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932095"
---
# <a name="animation-design"></a><span data-ttu-id="98c55-103">動畫設計</span><span class="sxs-lookup"><span data-stu-id="98c55-103">Animation Design</span></span>

<span data-ttu-id="98c55-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="98c55-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="98c55-105">影像設計</span><span class="sxs-lookup"><span data-stu-id="98c55-105">Image Design</span></span>

<span data-ttu-id="98c55-106">設計您的字元時，請使用 Microsoft Office 調色板，以將任何可能的調色板實現問題降至最低。</span><span class="sxs-lookup"><span data-stu-id="98c55-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="98c55-107">請避免選取與您在檔中使用的色彩類似的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="98c55-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="98c55-108">音效</span><span class="sxs-lookup"><span data-stu-id="98c55-108">Sounds</span></span>

<span data-ttu-id="98c55-109">Microsoft 代理程式可讓您在動畫中播放音效。</span><span class="sxs-lookup"><span data-stu-id="98c55-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="98c55-110">建議您不要包含 **閒置** 動畫的音效。</span><span class="sxs-lookup"><span data-stu-id="98c55-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="98c55-111">這是因為如果 Agent 必須載入系統多媒體 DLL，則動畫中間不會有延遲。</span><span class="sxs-lookup"><span data-stu-id="98c55-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="98c55-112">畫面格大小</span><span class="sxs-lookup"><span data-stu-id="98c55-112">Frame Size</span></span>

<span data-ttu-id="98c55-113">典型的辦公室助理為 123 x 93 圖元。</span><span class="sxs-lookup"><span data-stu-id="98c55-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="98c55-114">雖然您可以建立其他大小的字元，但它們會在助理資源庫中調整為 123 x 93。</span><span class="sxs-lookup"><span data-stu-id="98c55-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="98c55-115">框架轉換</span><span class="sxs-lookup"><span data-stu-id="98c55-115">Frame Transition</span></span>

<span data-ttu-id="98c55-116">除了 **再見**、 **問候**、 **顯示** 和 **隱藏** 以外的所有動畫，都應該以 RestPose 動畫作為開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="98c55-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="98c55-117">Microsoft Office 不會 **播放明確的** 傳回動畫，因此您不應該定義它們。</span><span class="sxs-lookup"><span data-stu-id="98c55-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="98c55-118">所有動畫也都應該有結束分支。</span><span class="sxs-lookup"><span data-stu-id="98c55-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="98c55-119">「結束分支」可讓我們在呼叫下一個動畫之前，先「趕上並完成」目前的動畫。</span><span class="sxs-lookup"><span data-stu-id="98c55-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="98c55-120">如果您未提供結束分支，則動畫之間的轉換可能會停用。</span><span class="sxs-lookup"><span data-stu-id="98c55-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="98c55-121">字元屬性</span><span class="sxs-lookup"><span data-stu-id="98c55-121">Character Properties</span></span>

<span data-ttu-id="98c55-122">Microsoft 代理程式可讓您設定字元的 [**名稱**](name-property.md)、 [**描述**](description-property.md) 及 [**ExtraData**](extradata-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="98c55-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="98c55-123">Microsoft Office 使用 **ExtraData** 欄位來保存一或多個簡介片語和提醒片語。</span><span class="sxs-lookup"><span data-stu-id="98c55-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="98c55-124">Microsoft Office 從其他簡介片語中挑選，以放入助理資源庫中的語音氣球。</span><span class="sxs-lookup"><span data-stu-id="98c55-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="98c55-125">當您收到 Outlook 的提醒時，我們會使用提醒片語。</span><span class="sxs-lookup"><span data-stu-id="98c55-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="98c55-126">[**ExtraData**](extradata-property.md)欄位的格式如下：</span><span class="sxs-lookup"><span data-stu-id="98c55-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="98c55-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="98c55-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="98c55-128">簡介片語會以成對的波狀字元字元分隔， (~) ，後面接著提醒片語。</span><span class="sxs-lookup"><span data-stu-id="98c55-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="98c55-129">這些提醒片語也會以成對的波狀字元字元分隔。</span><span class="sxs-lookup"><span data-stu-id="98c55-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="98c55-130">這兩組片語會以兩個插入號字元分隔 (^^) 。</span><span class="sxs-lookup"><span data-stu-id="98c55-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="98c55-131">每一種片語的數目都沒有限制，不同之處在于每個片語都必須至少有一個。</span><span class="sxs-lookup"><span data-stu-id="98c55-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 




