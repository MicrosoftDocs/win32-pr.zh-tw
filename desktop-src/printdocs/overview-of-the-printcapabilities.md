---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: PrintCapabilities 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ac6de8276c275fab05b728054b6f9a4e50e9bd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106988119"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="11b49-104">PrintCapabilities 總覽</span><span class="sxs-lookup"><span data-stu-id="11b49-104">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="11b49-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="11b49-105">This topic is not current.</span></span> <span data-ttu-id="11b49-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="11b49-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11b49-107">PrintCapabilities 描述裝置上可用的設定或狀態。</span><span class="sxs-lookup"><span data-stu-id="11b49-107">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="11b49-108">PrintCapabilities 所描述的裝置通常可以放在許多不同的設定中。</span><span class="sxs-lookup"><span data-stu-id="11b49-108">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="11b49-109">在列印裝置的情況下，一般列印屬性包含雙工列印、解析度和媒體大小。</span><span class="sxs-lookup"><span data-stu-id="11b49-109">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="11b49-110">如果裝置支援這些屬性，它們就是該裝置設定的一部分。</span><span class="sxs-lookup"><span data-stu-id="11b49-110">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="11b49-111">使用者藉由指派特定的值給每個可用的屬性，來選取特定的設定;例如，雙工： OneSided、解析度： 600 DPI 和 MediaSize：法律聲明。</span><span class="sxs-lookup"><span data-stu-id="11b49-111">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="11b49-112">PrintCapabilities 建置於 Print Schema Framework 上，其定義可在 PrintCapabilities 中使用的元素。</span><span class="sxs-lookup"><span data-stu-id="11b49-112">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="11b49-113">Print Schema 關鍵字會定義常用的元素階層或關鍵字，以促進個別用戶端之間資訊和意圖的可攜性。</span><span class="sxs-lookup"><span data-stu-id="11b49-113">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="11b49-114">不過，Print Schema 關鍵字也允許私用延伸模組，以便您可以根據特定需求量身訂做 PrintCapabilities。</span><span class="sxs-lookup"><span data-stu-id="11b49-114">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11b49-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="11b49-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11b49-116">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="11b49-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



