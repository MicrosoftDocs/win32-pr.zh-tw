---
description: 多媒體串流的優點
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: 多媒體串流的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116041"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="fcd62-103">多媒體串流的優點</span><span class="sxs-lookup"><span data-stu-id="fcd62-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="fcd62-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="fcd62-104">These APIs are deprecated.</span></span> <span data-ttu-id="fcd62-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="fcd62-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="fcd62-106">當開發人員在其應用程式中使用多媒體串流時，可以大幅減少所需的格式特定程式設計。</span><span class="sxs-lookup"><span data-stu-id="fcd62-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="fcd62-107">一般而言，必須從檔案或硬體來源取得媒體資料的應用程式，必須知道資料格式和硬體裝置的所有相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fcd62-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="fcd62-108">應用程式必須處理連接、資料傳輸、任何必要的資料轉換，以及實際的資料轉譯或檔案儲存體。</span><span class="sxs-lookup"><span data-stu-id="fcd62-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="fcd62-109">因為每種格式和裝置都稍微不同，所以此程式通常很複雜而且很麻煩。</span><span class="sxs-lookup"><span data-stu-id="fcd62-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="fcd62-110">另一方面，多媒體串流會自動協調將資料從來源傳送和轉換至應用程式的工作。</span><span class="sxs-lookup"><span data-stu-id="fcd62-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="fcd62-111">串流介面提供一致且可預測的資料存取和控制方法，可讓應用程式輕鬆地播放資料（不論其原始來源或格式為何）。</span><span class="sxs-lookup"><span data-stu-id="fcd62-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="fcd62-112">下列步驟說明如何執行串流，從硬體裝置到轉譯的播放。</span><span class="sxs-lookup"><span data-stu-id="fcd62-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="fcd62-113">影片資料的來源（例如 DirectShow）會公開串流介面。</span><span class="sxs-lookup"><span data-stu-id="fcd62-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="fcd62-114">應用程式開發人員會使用多媒體串流介面來處理資料格式轉換。</span><span class="sxs-lookup"><span data-stu-id="fcd62-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="fcd62-115">應用程式開發人員會使用 DirectDraw 介面來轉譯產生的資料。</span><span class="sxs-lookup"><span data-stu-id="fcd62-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="fcd62-116">多媒體串流的規格包含數個介面;每個介面都包含可控制串流處理常式特定層面或處理特定資料類型的方法。</span><span class="sxs-lookup"><span data-stu-id="fcd62-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="fcd62-117">如需其他資訊，請參閱 [多媒體串流介面的清單](list-of-multimedia-streaming-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="fcd62-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcd62-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcd62-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcd62-119">關於多媒體串流架構</span><span class="sxs-lookup"><span data-stu-id="fcd62-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



