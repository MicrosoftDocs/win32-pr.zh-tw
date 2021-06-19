---
description: PrintCapabilities 描述可在裝置上使用的設定或狀態，這些設定或狀態通常會放在一些不同的設定中。
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: PrintCapabilities 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8f61d1ee4125a9a1ac5f9ddb07cf226cd7094e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408521"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="5d4b2-103">PrintCapabilities 總覽</span><span class="sxs-lookup"><span data-stu-id="5d4b2-103">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="5d4b2-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-104">This topic is not current.</span></span> <span data-ttu-id="5d4b2-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5d4b2-106">PrintCapabilities 描述裝置上可用的設定或狀態。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-106">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="5d4b2-107">PrintCapabilities 所描述的裝置通常可以放在許多不同的設定中。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-107">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="5d4b2-108">在列印裝置的情況下，一般列印屬性包含雙工列印、解析度和媒體大小。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-108">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="5d4b2-109">如果裝置支援這些屬性，它們就是該裝置設定的一部分。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-109">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="5d4b2-110">使用者藉由指派特定的值給每個可用的屬性，來選取特定的設定;例如，雙工： OneSided、解析度： 600 DPI 和 MediaSize：法律聲明。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-110">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="5d4b2-111">PrintCapabilities 建置於 Print Schema Framework 上，其定義可在 PrintCapabilities 中使用的元素。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-111">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="5d4b2-112">Print Schema 關鍵字會定義常用的元素階層或關鍵字，以促進個別用戶端之間資訊和意圖的可攜性。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-112">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="5d4b2-113">不過，Print Schema 關鍵字也允許私用延伸模組，以便您可以根據特定需求量身訂做 PrintCapabilities。</span><span class="sxs-lookup"><span data-stu-id="5d4b2-113">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d4b2-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d4b2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d4b2-115">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5d4b2-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



