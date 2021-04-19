---
title: 建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式
description: 建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Windows Media Player 行動裝置、外掛程式
- Windows Media Player 行動裝置、使用者介面外掛程式
- Windows Media Player Mobile 外掛程式
- 外掛程式，使用者介面
- 外掛程式，Windows Media Player Mobile
- 使用者介面外掛程式，Windows Media Player Mobile
- UI 外掛程式，Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967827"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="917ea-110">建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式</span><span class="sxs-lookup"><span data-stu-id="917ea-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="917ea-111">Windows Media Player 10 行動裝置版會使用與桌面 Windows Media Player 相同的 UI 外掛程式模型。</span><span class="sxs-lookup"><span data-stu-id="917ea-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="917ea-112">不過，Windows Media Player 10 Mobile 只能與背景 UI 外掛程式互動。因為有類似的外掛程式模型，所以同樣適用于桌面上背景 UI 外掛程式的 API 呼叫也會套用至 Windows Mobile 裝置上的背景 UI 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="917ea-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="917ea-113">下列各節說明如何使用 Windows Media Player 外掛程式 Wizard 中的 wizard 產生的程式碼，建立背景 UI 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="917ea-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="917ea-114">區段</span><span class="sxs-lookup"><span data-stu-id="917ea-114">Section</span></span>                                                                | <span data-ttu-id="917ea-115">描述</span><span class="sxs-lookup"><span data-stu-id="917ea-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="917ea-116">快速入門</span><span class="sxs-lookup"><span data-stu-id="917ea-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="917ea-117">描述您需要安裝的內容，以及如何使用 Windows Media Player 外掛程式嚮導來協助自動化背景 UI 外掛程式的建立。</span><span class="sxs-lookup"><span data-stu-id="917ea-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="917ea-118">修改 Wizard 產生的程式碼</span><span class="sxs-lookup"><span data-stu-id="917ea-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="917ea-119">描述您需要從在上一節中建立的 wizard 產生程式碼中修改的內容，使其可與 Windows Media Player 10 行動裝置版搭配使用。</span><span class="sxs-lookup"><span data-stu-id="917ea-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="917ea-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="917ea-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="917ea-121">**消費者介面外掛程式程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="917ea-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




