---
description: 瞭解如何在 DirectShow 中建立 ASF 檔案。 ASF 是一種容器格式，可包含任何類型的資料。
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: 在 DirectShow (DirectShow) 中建立 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4614ed813c2e9f51c77cd8773739188aa5d4d07
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403962"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="07d1f-104">在 DirectShow (DirectShow) 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="07d1f-104">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="07d1f-105">本節說明如何使用 DirectShow [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器，以 Advanced Systems FORMAT (ASF) 來建立檔案。</span><span class="sxs-lookup"><span data-stu-id="07d1f-105">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="07d1f-106">ASF 是一種容器格式，可包含任何類型的壓縮或未壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="07d1f-106">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="07d1f-107">Windows Media 格式檔案是一種 ASF 檔案，使用 Windows Media Format 軟體發展工具組 (SDK) 中指定的特定編解碼器。</span><span class="sxs-lookup"><span data-stu-id="07d1f-107">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="07d1f-108">這些檔案會針對 Windows Media 音訊檔案使用副檔名 ".wma"，Windows Media 視訊檔案使用 ".wmv"。</span><span class="sxs-lookup"><span data-stu-id="07d1f-108">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="07d1f-109">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="07d1f-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="07d1f-110">DirectShow SDK 和 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="07d1f-110">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="07d1f-111">設定 ASF 寫入器</span><span class="sxs-lookup"><span data-stu-id="07d1f-111">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="07d1f-112">建立篩選圖形來寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="07d1f-112">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="07d1f-113">設定設定檔和其他 ASF 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="07d1f-113">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="07d1f-114">解除鎖定 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="07d1f-114">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="07d1f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="07d1f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d1f-116">在 DirectShow 中使用 Windows Media</span><span class="sxs-lookup"><span data-stu-id="07d1f-116">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



