---
description: 以功能/選項結構或參數表示屬性。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: 將屬性工作表示為功能/選項結構或參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120053"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="292e2-105">將屬性工作表示為功能/選項結構或參數</span><span class="sxs-lookup"><span data-stu-id="292e2-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="292e2-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="292e2-106">This topic is not current.</span></span> <span data-ttu-id="292e2-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="292e2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="292e2-108">PrintCapabilities 檔的作者會定義組成設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="292e2-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="292e2-109">在 PrintCapabilities 檔中，作者可以選擇將裝置屬性工作表示為功能/選項結構或參數結構。</span><span class="sxs-lookup"><span data-stu-id="292e2-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="292e2-110">如果裝置屬性有相對較少的可能狀態，而不屬於任何明顯的模式，則功能/選項結構通常是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="292e2-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="292e2-111">例如，如果 PageMediaSize 裝置屬性的允許值為字母、合法、A4ISO、Tabloid 和 Envelope10，則功能/選項結構會是標記法的較佳選擇。</span><span class="sxs-lookup"><span data-stu-id="292e2-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="292e2-112">由於與表示允許值沒有明確列舉相關聯的困難和不明確，因此參數結構不適合 PageMediaSize 屬性。</span><span class="sxs-lookup"><span data-stu-id="292e2-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="292e2-113">如果裝置屬性可由整數範圍表示，參數表示通常是較佳的選擇，特別是包含許多值的範圍。</span><span class="sxs-lookup"><span data-stu-id="292e2-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="292e2-114">例如，如果特定印表機模型的 CopyCount 裝置屬性可以範圍從1到99999，則應該藉由定義 ParameterDef 實例將此屬性分類為參數。</span><span class="sxs-lookup"><span data-stu-id="292e2-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="292e2-115">將值指派給 ParameterDef 專案的 MinValue 和 int32.maxvalue 標準屬性實例，以定義 JobCopyCount 屬性的值範圍。</span><span class="sxs-lookup"><span data-stu-id="292e2-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="292e2-116">由於必須明確地列為 Option 元素的大量值，因此功能/選項表示不適合 JobCopyCount 裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="292e2-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="292e2-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="292e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="292e2-118">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="292e2-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



