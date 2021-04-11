---
title: 修改 Echo 範例屬性頁
description: 修改 Echo 範例屬性頁
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372066"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="b4cac-108">修改 Echo 範例屬性頁</span><span class="sxs-lookup"><span data-stu-id="b4cac-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="b4cac-109">Windows Media Player 外掛程式 Wizard 的 DSP 外掛程式範例所提供的預設屬性頁執行，包含單一編輯方塊控制項，可接收使用者的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="b4cac-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="b4cac-110">您必須修改屬性頁，以接收 Echo 範例所使用的兩個屬性值。</span><span class="sxs-lookup"><span data-stu-id="b4cac-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="b4cac-111">如需有關 DSP 外掛程式屬性頁的總覽，請參閱 [執行音訊 DSP 外掛程式](implementing-an-audio-dsp-plug-in.md)。</span><span class="sxs-lookup"><span data-stu-id="b4cac-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="b4cac-112">下列各節將逐步引導您完成修改範例屬性頁的程式：</span><span class="sxs-lookup"><span data-stu-id="b4cac-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="b4cac-113">修改 Echo 對話資源</span><span class="sxs-lookup"><span data-stu-id="b4cac-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="b4cac-114">新增和修改事件</span><span class="sxs-lookup"><span data-stu-id="b4cac-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="b4cac-115">Echo 範例如何保存資料</span><span class="sxs-lookup"><span data-stu-id="b4cac-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="b4cac-116">執行 CEchoPropPage：： OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="b4cac-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="b4cac-117">執行 CEchoPropPage：： Apply</span><span class="sxs-lookup"><span data-stu-id="b4cac-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="b4cac-118">執行 CEcho：： FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="b4cac-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="b4cac-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4cac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4cac-120">**Echo 範例**</span><span class="sxs-lookup"><span data-stu-id="b4cac-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




