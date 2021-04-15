---
description: DirectShow 中的 DVD 解碼開發
ms.assetid: c00ff132-fee1-47b5-8a8a-df7cb920ad89
title: DirectShow 中的 DVD 解碼開發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3de64b3c1d91dbf5f22ba3e4b4ae8fe78edda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467869"
---
# <a name="dvd-decoder-development-in-directshow"></a><span data-ttu-id="04224-103">DirectShow 中的 DVD 解碼開發</span><span class="sxs-lookup"><span data-stu-id="04224-103">DVD Decoder Development in DirectShow</span></span>

<span data-ttu-id="04224-104">本節包含所有 DirectShow 屬性集的參考頁指標，以及 dvd 解碼中廣泛使用的介面。</span><span class="sxs-lookup"><span data-stu-id="04224-104">This section contains pointers to the reference pages for all the DirectShow property sets and interfaces that are either DVD-specific or else used extensively in DVD decoding.</span></span> <span data-ttu-id="04224-105">除了此處所列的內容之外，解碼器及其 pin 也必須支援一般的 DirectShow 篩選介面，如 [撰寫 DirectShow 篩選器](writing-directshow-filters.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="04224-105">In addition to what is listed here, a decoder and its pins must also support the generic DirectShow filter interfaces as described in [Writing DirectShow Filters](writing-directshow-filters.md).</span></span>

<span data-ttu-id="04224-106">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="04224-106">This section contains the following topics.</span></span>

-   [<span data-ttu-id="04224-107">解碼器磁片區控制</span><span class="sxs-lookup"><span data-stu-id="04224-107">Decoder Volume Control</span></span>](decoder-volume-control.md)
-   [<span data-ttu-id="04224-108">Windows 中的 DVD 區域變更支援</span><span class="sxs-lookup"><span data-stu-id="04224-108">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)

<span data-ttu-id="04224-109">另請參閱：</span><span class="sxs-lookup"><span data-stu-id="04224-109">See also:</span></span>

-   [<span data-ttu-id="04224-110">**DVD 卡拉卡拉屬性集**</span><span class="sxs-lookup"><span data-stu-id="04224-110">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="04224-111">**DVD 禁止複製屬性集**</span><span class="sxs-lookup"><span data-stu-id="04224-111">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="04224-112">**DVD 子圖片屬性集**</span><span class="sxs-lookup"><span data-stu-id="04224-112">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="04224-113">釘選屬性集</span><span class="sxs-lookup"><span data-stu-id="04224-113">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="04224-114">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="04224-114">**IKsPropertySet**</span></span>](ikspropertyset.md)
-   <span data-ttu-id="04224-115">僅) [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (硬體解碼器</span><span class="sxs-lookup"><span data-stu-id="04224-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (hardware decoders only)</span></span>
-   <span data-ttu-id="04224-116">僅) [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (硬體解碼器</span><span class="sxs-lookup"><span data-stu-id="04224-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (hardware decoders only)</span></span>

## <a name="related-topics"></a><span data-ttu-id="04224-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="04224-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04224-118">解碼器介面和規格</span><span class="sxs-lookup"><span data-stu-id="04224-118">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



