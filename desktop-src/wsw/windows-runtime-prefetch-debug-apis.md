---
title: 適用于 Windows Store 應用程式的預先提取偵錯工具 Api
description: 下列 Api 可用來在執行 ContentPrefetcher 類別的 Windows Store 應用程式中，對內容預先提取行為進行偵測和測試。
ms.assetid: 4FEB0320-7BE4-4B81-A9A1-C1FB5014A4BD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907cb44382f25e53ce9d4243539f5a7af3247a82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375945"
---
# <a name="prefetch-debug-apis-for-windows-store-apps"></a><span data-ttu-id="0014b-103">適用于 Windows Store 應用程式的預先提取偵錯工具 Api</span><span class="sxs-lookup"><span data-stu-id="0014b-103">Prefetch debug APIs for Windows Store apps</span></span>

<span data-ttu-id="0014b-104">下列 Api 可用來在執行 [**ContentPrefetcher**](/uwp/api/Windows.Networking.BackgroundTransfer.ContentPrefetcher) 類別的 Windows Store 應用程式中，對內容預先提取行為進行偵測和測試。</span><span class="sxs-lookup"><span data-stu-id="0014b-104">The following APIs are used to debug and test content prefetching behavior in a Windows Store app that implements the [**ContentPrefetcher**](/uwp/api/Windows.Networking.BackgroundTransfer.ContentPrefetcher) class.</span></span>



| <span data-ttu-id="0014b-105">介面</span><span class="sxs-lookup"><span data-stu-id="0014b-105">Interface</span></span>                                                              | <span data-ttu-id="0014b-106">描述</span><span class="sxs-lookup"><span data-stu-id="0014b-106">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0014b-107">**IContentPrefetcherTaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="0014b-107">**IContentPrefetcherTaskTrigger**</span></span>](/windows/desktop/api/IContentPrefetcherTaskTrigger/nn-icontentprefetchertasktrigger-icontentprefetchertasktrigger) | <span data-ttu-id="0014b-108">使用此介面來確認已針對此背景工作註冊已安裝的 Windows Store 應用程式套件，並手動觸發其內容預先提取作業。</span><span class="sxs-lookup"><span data-stu-id="0014b-108">Use this interface to verify that an installed Windows Store app package is registered for this background task and manually trigger its content prefetch operations.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0014b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="0014b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0014b-110">**ContentPrefetcher**</span><span class="sxs-lookup"><span data-stu-id="0014b-110">**ContentPrefetcher**</span></span>](/uwp/api/Windows.Networking.BackgroundTransfer.ContentPrefetcher)
</dt> </dl>

 

