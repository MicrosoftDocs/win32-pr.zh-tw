---
description: 瞭解如何參考參數和 ParameterDef 元素。 包含 ParameterRef 元素的選項範例是自訂媒體大小選項。
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: 參考參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405321"
---
# <a name="referencing-parameters"></a><span data-ttu-id="a266f-104">參考參數</span><span class="sxs-lookup"><span data-stu-id="a266f-104">Referencing Parameters</span></span>

<span data-ttu-id="a266f-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a266f-105">This topic is not current.</span></span> <span data-ttu-id="a266f-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a266f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a266f-107">包含 ParameterRef 元素之選項的具體範例是自訂媒體大小選項。</span><span class="sxs-lookup"><span data-stu-id="a266f-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="a266f-108">請注意，它會參考兩個參數： PageMediaSizeMediaSizeWidth 和 PageMediaSizeMediaSizeHeight。</span><span class="sxs-lookup"><span data-stu-id="a266f-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="a266f-109">每個 ParameterRef 實例都會參考 PrintCapabilities 檔中其他位置所定義的 ParameterDef 實例。</span><span class="sxs-lookup"><span data-stu-id="a266f-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="a266f-110">如需 ParameterDef 元素的詳細資訊，請參閱 [ParameterDef](parameterdef.md)。</span><span class="sxs-lookup"><span data-stu-id="a266f-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="a266f-111">如需有關定義參數的概念資訊，請參閱 [ParameterDef 和 ParameterInit 元素](parameterdef-and-parameterinit-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="a266f-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="a266f-112">只是要建立參數化選項，以確保會正確處理和處理選項。</span><span class="sxs-lookup"><span data-stu-id="a266f-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="a266f-113">PrintCapabilities/PrintTicket 提供者和用戶端必須提供其他支援，才能正確地執行參數化選項實例。</span><span class="sxs-lookup"><span data-stu-id="a266f-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="a266f-114">下列各節將說明所需的行為。</span><span class="sxs-lookup"><span data-stu-id="a266f-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a266f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a266f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a266f-116">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a266f-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



