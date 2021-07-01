---
description: 瞭解 PrintCapabilities 檔中的參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: PrintCapabilities 檔中的參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118623"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="c805f-105">PrintCapabilities 檔中的參數</span><span class="sxs-lookup"><span data-stu-id="c805f-105">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="c805f-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c805f-106">This topic is not current.</span></span> <span data-ttu-id="c805f-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c805f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c805f-108">如 [參數參考](parameter-reference-elements.md)專案中所述，可從選項實例中參考 ParameterInit 元素，但參數結構也具有與這種類型的元素無關的用途。</span><span class="sxs-lookup"><span data-stu-id="c805f-108">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="c805f-109">裝置設定屬性的範例，很適合用於參數標記法 CopyCount。</span><span class="sxs-lookup"><span data-stu-id="c805f-109">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="c805f-110">您可以輕鬆且精確地定義此裝置設定屬性的允許值，而不需要明確列出每個值。</span><span class="sxs-lookup"><span data-stu-id="c805f-110">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="c805f-111">雖然有可能是很繁瑣的，若要在自己的選項中列出每個 CopyCount 值，某些裝置設定屬性就無法使用功能/選項結構來表示。</span><span class="sxs-lookup"><span data-stu-id="c805f-111">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="c805f-112">例如，假設有一個裝置接受文字字串，然後用來在每個輸出頁面上產生虛擬水位線。</span><span class="sxs-lookup"><span data-stu-id="c805f-112">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="c805f-113">所有可能的文字字串集合都無法輕易地明確列舉，但是可以使用 ParameterDef 元素輕鬆描述文字字串。</span><span class="sxs-lookup"><span data-stu-id="c805f-113">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="c805f-114">Print Schema 關鍵字檔會定義許多常用的參數結構，但 PrintCapabilities 提供者可自由定義自己的其他專案。</span><span class="sxs-lookup"><span data-stu-id="c805f-114">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="c805f-115">不過，這些私用定義的參數結構無法移植到其他裝置，因為另一方提供的 PrintCapabilities 檔不會定義這類參數結構。</span><span class="sxs-lookup"><span data-stu-id="c805f-115">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="c805f-116">無論是架構定義或私下定義，ParameterDef 實例都必須存在於 PrintCapabilities 檔中，用戶端才能辨識並使用參數。</span><span class="sxs-lookup"><span data-stu-id="c805f-116">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="c805f-117">這些參數稱為 *指定的參數*。</span><span class="sxs-lookup"><span data-stu-id="c805f-117">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c805f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c805f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c805f-119">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c805f-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



