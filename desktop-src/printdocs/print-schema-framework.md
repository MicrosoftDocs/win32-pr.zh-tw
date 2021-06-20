---
description: 這些文章提供有關列印架構元素類型之意義和使用方式的詳細資訊。
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Print Schema Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407161"
---
# <a name="print-schema-framework"></a><span data-ttu-id="c8b74-103">Print Schema Framework</span><span class="sxs-lookup"><span data-stu-id="c8b74-103">Print Schema Framework</span></span>

<span data-ttu-id="c8b74-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c8b74-104">This topic is not current.</span></span> <span data-ttu-id="c8b74-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c8b74-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c8b74-106">本節提供有關列印架構元素類型之意義和使用方式的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c8b74-106">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="c8b74-107">列印架構架構初始版本的主要重點在於代表裝置屬性的設定和功能。</span><span class="sxs-lookup"><span data-stu-id="c8b74-107">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="c8b74-108">概括而言，此架構提供兩種不同的樣式來描述裝置屬性：做為功能/選項結構，或做為參數結構。</span><span class="sxs-lookup"><span data-stu-id="c8b74-108">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="c8b74-109">如果裝置屬性有少量的可用值或狀態，則屬性的特性應該是具有允許的值或狀態（稱為 Option 元素）的特徵。</span><span class="sxs-lookup"><span data-stu-id="c8b74-109">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="c8b74-110">相反地，如果裝置屬性有大量可用的值或狀態，而且您可以輕鬆地定義所有可能值的集合，而不需要使用明確列舉，則裝置屬性應該是參數的特性。</span><span class="sxs-lookup"><span data-stu-id="c8b74-110">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="c8b74-111"> (參數是透過 ParameterDef 元素來定義，而參數實例則是透過 ParameterInit 專案來初始化。 ) 屬性專案會在功能/選項和參數結構內使用，以提供更細微的差異層級。</span><span class="sxs-lookup"><span data-stu-id="c8b74-111">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8b74-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8b74-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8b74-113">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c8b74-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



