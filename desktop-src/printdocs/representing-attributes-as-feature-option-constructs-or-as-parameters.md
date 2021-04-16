---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: 將屬性工作表示為功能/選項結構或參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104027698"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="1ba57-104">將屬性工作表示為功能/選項結構或參數</span><span class="sxs-lookup"><span data-stu-id="1ba57-104">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="1ba57-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1ba57-105">This topic is not current.</span></span> <span data-ttu-id="1ba57-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1ba57-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1ba57-107">PrintCapabilities 檔的作者會定義組成設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="1ba57-107">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="1ba57-108">在 PrintCapabilities 檔中，作者可以選擇將裝置屬性工作表示為功能/選項結構或參數結構。</span><span class="sxs-lookup"><span data-stu-id="1ba57-108">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="1ba57-109">如果裝置屬性有相對較少的可能狀態，而不屬於任何明顯的模式，則功能/選項結構通常是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="1ba57-109">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="1ba57-110">例如，如果 PageMediaSize 裝置屬性的允許值為字母、合法、A4ISO、Tabloid 和 Envelope10，則功能/選項結構會是標記法的較佳選擇。</span><span class="sxs-lookup"><span data-stu-id="1ba57-110">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="1ba57-111">由於與表示允許值沒有明確列舉相關聯的困難和不明確，因此參數結構不適合 PageMediaSize 屬性。</span><span class="sxs-lookup"><span data-stu-id="1ba57-111">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="1ba57-112">如果裝置屬性可由整數範圍表示，參數表示通常是較佳的選擇，特別是包含許多值的範圍。</span><span class="sxs-lookup"><span data-stu-id="1ba57-112">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="1ba57-113">例如，如果特定印表機模型的 CopyCount 裝置屬性可以範圍從1到99999，則應該藉由定義 ParameterDef 實例將此屬性分類為參數。</span><span class="sxs-lookup"><span data-stu-id="1ba57-113">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="1ba57-114">將值指派給 ParameterDef 專案的 MinValue 和 int32.maxvalue 標準屬性實例，以定義 JobCopyCount 屬性的值範圍。</span><span class="sxs-lookup"><span data-stu-id="1ba57-114">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="1ba57-115">由於必須明確地列為 Option 元素的大量值，因此功能/選項表示不適合 JobCopyCount 裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="1ba57-115">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ba57-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ba57-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ba57-117">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1ba57-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



