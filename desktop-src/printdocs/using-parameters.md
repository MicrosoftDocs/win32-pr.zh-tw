---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: 使用參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fe8fc7c79ed27c467b59ef67132e816cdcd63
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195807"
---
# <a name="using-parameters"></a><span data-ttu-id="cad6a-104">使用參數</span><span class="sxs-lookup"><span data-stu-id="cad6a-104">Using Parameters</span></span>

<span data-ttu-id="cad6a-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="cad6a-105">This topic is not current.</span></span> <span data-ttu-id="cad6a-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="cad6a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cad6a-107">除了適當計分包含 ParameterRef 實例的選項 (請參閱) 、PrintCapabilities 或 PrintTicket 提供者的 [參考參數](referencing-parameters.md) ，以及用戶端必須準備好處理下列涉及參數的狀況。</span><span class="sxs-lookup"><span data-stu-id="cad6a-107">In addition to properly scoring an Option that contains ParameterRef instances (see [Referencing Parameters](referencing-parameters.md)), PrintCapabilities or PrintTicket providers and clients must be prepared to handle the following situations involving parameters.</span></span>

<span data-ttu-id="cad6a-108">使用者介面 (UI) 用戶端必須提示使用者提供參數初始化運算式 (值給適當時間的指定參數) ，以便將適當的 ParameterInit 元素插入至 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="cad6a-108">User interface (UI) clients must prompt the user to provide parameter initializers (values for ParameterInit elements) for designated parameters at the appropriate time so that the appropriate ParameterInit elements are inserted into the PrintTicket.</span></span> <span data-ttu-id="cad6a-109">UI 用戶端必須能夠區分這兩種類型的參數（無條件強制），並有條件地強制性，而且必須能夠適當地處理每個型別。</span><span class="sxs-lookup"><span data-stu-id="cad6a-109">UI clients must be able to distinguish the two types of parameters, unconditionally mandatory, and conditionally mandatory, and must be able to handle each type appropriately.</span></span> <span data-ttu-id="cad6a-110">若為無條件強制參數，UI 必須確保為此類型的參數提供 ParameterInit 元素。</span><span class="sxs-lookup"><span data-stu-id="cad6a-110">For an unconditionally mandatory parameter, the UI must ensure that a ParameterInit element is provided for this type of parameter.</span></span> <span data-ttu-id="cad6a-111">針對有條件的強制參數，如果在 PrintTicket 中選取的選項參考參數，則 UI 必須提供 ParameterInit 值。</span><span class="sxs-lookup"><span data-stu-id="cad6a-111">For a conditionally mandatory parameter, the UI must provide a ParameterInit value if the parameter is referenced by an Option that is selected in the PrintTicket.</span></span> <span data-ttu-id="cad6a-112">參數的強制狀態是在 ParameterDef 實例中指定。</span><span class="sxs-lookup"><span data-stu-id="cad6a-112">The Mandatory status of a parameter is specified in a ParameterDef instance.</span></span> <span data-ttu-id="cad6a-113">如需詳細資訊，請參閱 [ParameterDef 和 ParameterInit 元素](parameterdef-and-parameterinit-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="cad6a-113">For more information, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span> <span data-ttu-id="cad6a-114">UI 用戶端應該驗證使用者提供的 ParameterInit 值，以確認它們符合 ParameterDef 實例中指定的需求。</span><span class="sxs-lookup"><span data-stu-id="cad6a-114">UI clients should validate user-supplied ParameterInit values to verify that they satisfy the requirements specified in the ParameterDef instance.</span></span>

<span data-ttu-id="cad6a-115">PrintTicket 提供者也應該檢查 PrintTicket 提供的 ParameterInit 實例，以確認所有必要的參數都存在，而且它們滿足 ParameterDef 實例中指定的需求。</span><span class="sxs-lookup"><span data-stu-id="cad6a-115">PrintTicket providers should also check the ParameterInit instances supplied by the PrintTicket to verify that all needed parameters are present, and that they satisfy the requirements specified in the ParameterDef instance.</span></span> <span data-ttu-id="cad6a-116">當 ParameterInit 值無效或遺失時，驗證程式代碼應該提供合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="cad6a-116">The validation code should supply reasonable defaults in the event that ParameterInit values are invalid or missing.</span></span> <span data-ttu-id="cad6a-117">請注意，ParameterDef 允許針對此用途提供預設值。</span><span class="sxs-lookup"><span data-stu-id="cad6a-117">Notice that a ParameterDef permits a default value to be supplied for this purpose.</span></span> <span data-ttu-id="cad6a-118">此外，如果有涉及參數的條件約束，例如「如果 *CopyCount* 大於 N，則請勿使用小型容量輸入 bin」。「PrintTicket 驗證程式代碼應該偵測到此條件約束，並修改 printticket 以避免啟用條件約束。</span><span class="sxs-lookup"><span data-stu-id="cad6a-118">Also, if there are constraints involving the parameters, for example, "if *CopyCount* is larger than N, then do not use a small capacity input bin," the PrintTicket validation code should detect this constraint and modify the PrintTicket to avoid activating the constraint.</span></span>

<span data-ttu-id="cad6a-119">如果在 PrintTicket 中指定的參數上有 PrintCapabilities 的相依性，PrintCapabilities 提供者必須監視 ParameterInit 值並產生適當的 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="cad6a-119">If there is any dependency of the PrintCapabilities on the parameters specified in the PrintTicket, PrintCapabilities providers must monitor the ParameterInit values and produce an appropriate PrintCapabilities document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cad6a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="cad6a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cad6a-121">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="cad6a-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



