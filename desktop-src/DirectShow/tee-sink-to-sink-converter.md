---
description: T/接收到接收轉換器
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: T/接收到接收轉換器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979820"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="d6708-103">T/接收到接收轉換器</span><span class="sxs-lookup"><span data-stu-id="d6708-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="d6708-104">端對端/接收到接收轉換器是以核心模式、KsProxy 為基礎的篩選。</span><span class="sxs-lookup"><span data-stu-id="d6708-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="d6708-105">它用於轉譯或捕獲 VBI 資料的類比視頻電視篩選圖形中。</span><span class="sxs-lookup"><span data-stu-id="d6708-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="d6708-106">篩選會連接上游至 [WDM 影片捕獲篩選器](wdm-video-capture-filter.md) ，並提供有效率的方法來複製核心模式中的資料流程，而不需要在核心和使用者模式之間進行昂貴的轉換。</span><span class="sxs-lookup"><span data-stu-id="d6708-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="d6708-107">它會將每個接收到的資料區塊傳遞給所有輸出圖釘，而下游編解碼器會負責尋找要解碼的特定 VBI 資料。</span><span class="sxs-lookup"><span data-stu-id="d6708-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="d6708-108">端對端對接收的轉換器會出現在「WDM 串流的 t/分隔裝置」篩選類別 (AM \_ KSCATEGORY \_ 分隔器) 。</span><span class="sxs-lookup"><span data-stu-id="d6708-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="d6708-109">由於這是核心模式篩選器，因此應用程式無法直接使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立它。</span><span class="sxs-lookup"><span data-stu-id="d6708-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="d6708-110">相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="d6708-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="d6708-111">如需詳細資訊，請參閱 [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="d6708-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6708-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6708-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6708-113">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="d6708-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
