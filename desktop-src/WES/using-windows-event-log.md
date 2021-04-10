---
title: 使用 Windows 事件記錄檔
description: 本節包含如何使用 Windows 事件記錄檔 API 撰寫檢測資訊清單、撰寫提供資訊清單中所定義之事件的提供者，以及取用所記錄事件的詳細資料。
ms.assetid: c2855190-584b-406d-acff-5ffbf10dbb5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8aca9896eabf1f785cef590993a0e6184f70c39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092780"
---
# <a name="using-windows-event-log"></a><span data-ttu-id="101f0-103">使用 Windows 事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="101f0-103">Using Windows Event Log</span></span>

<span data-ttu-id="101f0-104">本節包含如何使用 Windows 事件記錄檔 API 撰寫檢測資訊清單、撰寫提供資訊清單中所定義之事件的提供者，以及取用所記錄事件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="101f0-104">This section contains the details on how to use the Windows Event Log API to write an instrumentation manifest, write the provider that provides the events defined in the manifest, and consume the events that are logged.</span></span>

<span data-ttu-id="101f0-105">如需詳細資料，請參閱下列主題︰</span><span class="sxs-lookup"><span data-stu-id="101f0-105">For details, see the following topics:</span></span>

-   [<span data-ttu-id="101f0-106">撰寫檢測資訊清單</span><span class="sxs-lookup"><span data-stu-id="101f0-106">Writing an Instrumentation Manifest</span></span>](writing-an-instrumentation-manifest.md)
-   [<span data-ttu-id="101f0-107">編譯檢測資訊清單</span><span class="sxs-lookup"><span data-stu-id="101f0-107">Compiling an Instrumentation Manifest</span></span>](compiling-an-instrumentation-manifest.md)
-   [<span data-ttu-id="101f0-108">開發提供者</span><span class="sxs-lookup"><span data-stu-id="101f0-108">Developing a Provider</span></span>](developing-a-provider.md)
-   [<span data-ttu-id="101f0-109">使用事件</span><span class="sxs-lookup"><span data-stu-id="101f0-109">Consuming Events</span></span>](consuming-events.md)
-   [<span data-ttu-id="101f0-110">取得和設定通道的設定屬性</span><span class="sxs-lookup"><span data-stu-id="101f0-110">Getting and Setting a Channel's Configuration Properties</span></span>](getting-and-setting-a-channel-s-configuration-properties.md)
-   [<span data-ttu-id="101f0-111">取得提供者的中繼資料</span><span class="sxs-lookup"><span data-stu-id="101f0-111">Getting a Provider's Metadata</span></span>](getting-a-provider-s-metadata-.md)
-   [<span data-ttu-id="101f0-112">存取遠端電腦</span><span class="sxs-lookup"><span data-stu-id="101f0-112">Accessing Remote Computers</span></span>](accessing-remote-computers.md)
-   [<span data-ttu-id="101f0-113">將事件儲存至記錄檔</span><span class="sxs-lookup"><span data-stu-id="101f0-113">Saving Events to a Log File</span></span>](saving-events-to-a-log-file.md)

## <a name="related-topics"></a><span data-ttu-id="101f0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="101f0-114">Related topics</span></span>

[<span data-ttu-id="101f0-115">如何透過 Windows 事件記錄檔服務啟用 WPP 追蹤？</span><span class="sxs-lookup"><span data-stu-id="101f0-115">How Do I Enable WPP Tracing Through the Windows Event Log Service?</span></span>](/windows-hardware/drivers/devtest/enabling-wpp-tracing-through-windows-event-log)

[<span data-ttu-id="101f0-116">Windows 事件記錄檔參考</span><span class="sxs-lookup"><span data-stu-id="101f0-116">Windows Event Log Reference</span></span>](windows-event-log-reference.md)