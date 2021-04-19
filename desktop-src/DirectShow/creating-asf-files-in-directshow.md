---
description: 在 DirectShow 中建立 ASF 檔案
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: 在 DirectShow (DirectShow) 中建立 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f5c9ebac0b14b736c47599ee25a1c1c28dd8f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970304"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="bbc2a-103">在 DirectShow (DirectShow) 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="bbc2a-103">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="bbc2a-104">本節說明如何使用 DirectShow [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器，以 Advanced Systems FORMAT (ASF) 來建立檔案。</span><span class="sxs-lookup"><span data-stu-id="bbc2a-104">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="bbc2a-105">ASF 是一種容器格式，可包含任何類型的壓縮或未壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="bbc2a-105">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="bbc2a-106">Windows Media 格式檔案是一種 ASF 檔案，使用 Windows Media Format 軟體發展工具組 (SDK) 中指定的特定編解碼器。</span><span class="sxs-lookup"><span data-stu-id="bbc2a-106">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="bbc2a-107">這些檔案會針對 Windows Media 音訊檔案使用副檔名 ".wma"，Windows Media 視訊檔案使用 ".wmv"。</span><span class="sxs-lookup"><span data-stu-id="bbc2a-107">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="bbc2a-108">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="bbc2a-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="bbc2a-109">DirectShow SDK 和 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="bbc2a-109">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="bbc2a-110">設定 ASF 寫入器</span><span class="sxs-lookup"><span data-stu-id="bbc2a-110">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="bbc2a-111">建立篩選圖形來寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="bbc2a-111">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="bbc2a-112">設定設定檔和其他 ASF 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="bbc2a-112">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="bbc2a-113">解除鎖定 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="bbc2a-113">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="bbc2a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbc2a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc2a-115">在 DirectShow 中使用 Windows Media</span><span class="sxs-lookup"><span data-stu-id="bbc2a-115">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



