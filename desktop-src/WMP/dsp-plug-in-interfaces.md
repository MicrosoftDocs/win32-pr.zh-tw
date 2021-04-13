---
title: DSP 外掛程式介面
description: DSP 外掛程式介面
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player 外掛程式、DSP 介面
- Windows Media Player 外掛程式，介面
- 外掛程式、DSP 介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- 數位信號處理外掛程式，ISpecifyPropertyPage 介面
- DSP 外掛程式，介面
- DSP 外掛程式，ISpecifyPropertyPage 介面
- 介面、DSP 外掛程式
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104374765"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="1095e-113">DSP 外掛程式介面</span><span class="sxs-lookup"><span data-stu-id="1095e-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="1095e-114">數位信號處理 (DSP) 外掛程式介面，用來管理 Windows Media Player 和外掛程式之間的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="1095e-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="1095e-115">所有的 DSP 外掛程式都可以選擇性地執行 **ISpecifyPropertyPage** 介面，以提供屬性頁面的執行。</span><span class="sxs-lookup"><span data-stu-id="1095e-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="1095e-116">需要下列介面才能建立 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="1095e-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="1095e-117">介面</span><span class="sxs-lookup"><span data-stu-id="1095e-117">Interface</span></span>                                                | <span data-ttu-id="1095e-118">描述</span><span class="sxs-lookup"><span data-stu-id="1095e-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1095e-119">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="1095e-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="1095e-120">使用 Windows Media Player 管理資料交換，並執行數位信號處理工作。</span><span class="sxs-lookup"><span data-stu-id="1095e-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="1095e-121">DirectX SDK 包含詳細的檔。</span><span class="sxs-lookup"><span data-stu-id="1095e-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="1095e-122">IWMPMediaPluginRegistrar</span><span class="sxs-lookup"><span data-stu-id="1095e-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="1095e-123">管理外掛程式註冊。</span><span class="sxs-lookup"><span data-stu-id="1095e-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="1095e-124">IWMPPlugin</span><span class="sxs-lookup"><span data-stu-id="1095e-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="1095e-125">管理 Windows Media Player 的連接。</span><span class="sxs-lookup"><span data-stu-id="1095e-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="1095e-126">IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="1095e-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="1095e-127">儲存 Windows Media Player 目前是否已啟用外掛程式。</span><span class="sxs-lookup"><span data-stu-id="1095e-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="1095e-128">IWMPServices</span><span class="sxs-lookup"><span data-stu-id="1095e-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="1095e-129">從玩家抓取目前資料流程時間和資料流程狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1095e-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="1095e-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="1095e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1095e-131">**DSP 外掛程式程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="1095e-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




