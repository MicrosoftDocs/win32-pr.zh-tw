---
title: 使用 Windows Media Player 啟用同步處理
description: 使用 Windows Media Player 啟用同步處理
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media 裝置管理員，與 Windows Media Player 同步處理
- 裝置管理員，與 Windows Media Player 同步處理
- 程式設計指南，與 Windows Media Player 同步處理
- 服務提供者，與 Windows Media Player 同步處理
- 建立服務提供者，與 Windows Media Player 同步處理
- 與 Windows Media Player 同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965613"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="d77ec-109">使用 Windows Media Player 啟用同步處理</span><span class="sxs-lookup"><span data-stu-id="d77ec-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="d77ec-110">您可以讓裝置參與 Windows Media Player 的自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="d77ec-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="d77ec-111">自動同步處理表示當使用者指定的同步處理裝置連接到電腦時，Windows Media Player 會自動從裝置下載、更新或刪除檔案，而不需要任何額外的使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="d77ec-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="d77ec-112">根據預設，下列裝置會與 Windows Media Player 同步處理：</span><span class="sxs-lookup"><span data-stu-id="d77ec-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="d77ec-113">MTP 裝置</span><span class="sxs-lookup"><span data-stu-id="d77ec-113">MTP devices</span></span>
-   <span data-ttu-id="d77ec-114">大量儲存裝置</span><span class="sxs-lookup"><span data-stu-id="d77ec-114">Mass-storage devices</span></span>
-   <span data-ttu-id="d77ec-115">Windows CE (Windows Media Player 10 行動裝置版和更新版本的裝置) </span><span class="sxs-lookup"><span data-stu-id="d77ec-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="d77ec-116">針對要與 Windows Media Player 同步處理的任何其他裝置，必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="d77ec-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="d77ec-117">裝置必須公告為 {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE} 的 PAP 裝置介面</span><span class="sxs-lookup"><span data-stu-id="d77ec-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="d77ec-118">服務提供者所傳回的裝置物件必須支援 **IMDSPDevice3** 介面。</span><span class="sxs-lookup"><span data-stu-id="d77ec-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="d77ec-119">裝置參數 UseExtendedWmdm 必須設定為 **DWORD** 值1。</span><span class="sxs-lookup"><span data-stu-id="d77ec-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="d77ec-120">如需詳細資訊，請參閱 [裝置參數](device-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="d77ec-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="d77ec-121">服務提供者應該執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="d77ec-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="d77ec-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="d77ec-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="d77ec-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="d77ec-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="d77ec-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="d77ec-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="d77ec-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d77ec-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d77ec-126">**建立服務提供者**</span><span class="sxs-lookup"><span data-stu-id="d77ec-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="d77ec-127">**裝置參數**</span><span class="sxs-lookup"><span data-stu-id="d77ec-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




