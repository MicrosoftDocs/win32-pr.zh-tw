---
title: 音訊行和控制項查詢
description: 音訊行和控制項查詢
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- 多媒體音訊、混音器控制項
- 音訊、混音器控制項
- 音訊 mixers，音訊行
- 音訊行
- 音訊 mixers，控制項
- mixers，控制項
- mixers，音訊行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681804"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="1a7d5-110">音訊行和控制項查詢</span><span class="sxs-lookup"><span data-stu-id="1a7d5-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="1a7d5-111">混音器服務提供用來決定音訊行、音訊行控制項及控制項詳細資料相關資訊的功能。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="1a7d5-112">這些服務也會提供用來設定控制項詳細資料的功能。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="1a7d5-113">您可以使用 [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) 函式來取得指定之音訊行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="1a7d5-114">此函式會針對指定的來源音訊行、目的地音訊行或行識別碼填滿 [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) 結構。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="1a7d5-115">此結構包含目的地行號、音訊行中的通道數目，以及音訊行的簡短和完整名稱。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="1a7d5-116">[**MixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)函式會取得一或多個與音訊行相關聯之控制項的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="1a7d5-117">此函式會以指定的控制項或控制項的相關資訊填入 [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) 結構。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="1a7d5-118">您可以使用 **mixerGetLineControls** 來取出下列其中一項的控制項屬性：</span><span class="sxs-lookup"><span data-stu-id="1a7d5-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="1a7d5-119">指定之原始程式列的所有控制項</span><span class="sxs-lookup"><span data-stu-id="1a7d5-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="1a7d5-120">指定之原始程式列的指定控制項</span><span class="sxs-lookup"><span data-stu-id="1a7d5-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="1a7d5-121">指定原始程式列之特定類別的第一個控制項</span><span class="sxs-lookup"><span data-stu-id="1a7d5-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="1a7d5-122">[**MixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)函式會抓取與音訊行相關聯之單一控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="1a7d5-123">此函式會以控制項目前的值填入 [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) 結構。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="1a7d5-124">[**MixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)函式會使用 **MIXERCONTROLDETAILS** 結構的內容來設定指定之控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="1a7d5-125">在呼叫 **mixerSetControlDetails** 之前，您必須確定已填入此結構的所有成員。</span><span class="sxs-lookup"><span data-stu-id="1a7d5-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 