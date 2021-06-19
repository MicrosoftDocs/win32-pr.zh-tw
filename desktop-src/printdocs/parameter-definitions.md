---
description: 閱讀 PrintCapabilities 檔中有關參數定義的資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: 參數定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396573"
---
# <a name="parameter-definitions"></a><span data-ttu-id="61f4f-105">參數定義</span><span class="sxs-lookup"><span data-stu-id="61f4f-105">Parameter Definitions</span></span>

<span data-ttu-id="61f4f-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="61f4f-106">This topic is not current.</span></span> <span data-ttu-id="61f4f-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="61f4f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="61f4f-108">本節將概述可能出現在 PrintCapabilities 檔中的公用參數定義。</span><span class="sxs-lookup"><span data-stu-id="61f4f-108">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="61f4f-109">參數是用來描述可接受的值範圍，而不是值的離散列舉。</span><span class="sxs-lookup"><span data-stu-id="61f4f-109">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="61f4f-110">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="61f4f-110">ParameterDef</span></span>

<span data-ttu-id="61f4f-111">如需 ParameterDef 元素類型的摘要，請參閱 [ParameterDef](parameterdef.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="61f4f-111">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="61f4f-112">如需 ParameterDef 元素與 ParameterInit 專案之間互動的詳細資訊，請參閱 [ParameterDef 和 ParameterInit 元素](./parameterdef-and-parameterinit-elements.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="61f4f-112">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="61f4f-113">ParameterDef 在列印架構關鍵字中定義的元素必須在 PrintCapabilities 檔中完整定義。</span><span class="sxs-lookup"><span data-stu-id="61f4f-113">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="61f4f-114">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="61f4f-114">ParameterRef</span></span>

<span data-ttu-id="61f4f-115">如需 ParameterRef 元素類型的摘要，請參閱 [ParameterRef](parameterref.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="61f4f-115">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="61f4f-116">使用者可設定的元素關鍵字可以包含參數的參考。</span><span class="sxs-lookup"><span data-stu-id="61f4f-116">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="61f4f-117">ParameterRef 元素會指定為 ScoredProperty 專案的子系。如需詳細資訊，請參閱 [參數參考元素](parameter-reference-elements.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="61f4f-117">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61f4f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="61f4f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f4f-119">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="61f4f-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
