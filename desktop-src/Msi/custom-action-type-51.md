---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型51。
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: 自訂動作類型51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944847"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="6e700-103">自訂動作類型51</span><span class="sxs-lookup"><span data-stu-id="6e700-103">Custom Action Type 51</span></span>

<span data-ttu-id="6e700-104">此自訂動作會從格式化的文字字串設定屬性。</span><span class="sxs-lookup"><span data-stu-id="6e700-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="6e700-105">若要影響元件或功能的條件中所使用的屬性，自訂動作必須在動作順序中的 [CostFinalize 動作](costfinalize-action.md) 之前。</span><span class="sxs-lookup"><span data-stu-id="6e700-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="6e700-106">來源</span><span class="sxs-lookup"><span data-stu-id="6e700-106">Source</span></span>

<span data-ttu-id="6e700-107">[CustomAction 資料表](customaction-table.md)的來源欄位可以包含屬性的名稱或[屬性資料表](property-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6e700-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="6e700-108">這個屬性是由目標欄位中使用 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)的格式化字串所設定。</span><span class="sxs-lookup"><span data-stu-id="6e700-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="6e700-109">類型值</span><span class="sxs-lookup"><span data-stu-id="6e700-109">Type Value</span></span>

<span data-ttu-id="6e700-110">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="6e700-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="6e700-111">常數</span><span class="sxs-lookup"><span data-stu-id="6e700-111">Constants</span></span>                                                             | <span data-ttu-id="6e700-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="6e700-112">Hexadecimal</span></span> | <span data-ttu-id="6e700-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="6e700-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="6e700-114">**msidbCustomActionTypeTextData**  + **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="6e700-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="6e700-115">0x033</span><span class="sxs-lookup"><span data-stu-id="6e700-115">0x033</span></span>       | <span data-ttu-id="6e700-116">51</span><span class="sxs-lookup"><span data-stu-id="6e700-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="6e700-117">目標</span><span class="sxs-lookup"><span data-stu-id="6e700-117">Target</span></span>

<span data-ttu-id="6e700-118">[CustomAction 資料表](customaction-table.md)的目標資料行包含使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (中指定的功能來格式化的文字字串，而不含數值欄位規範) 。</span><span class="sxs-lookup"><span data-stu-id="6e700-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="6e700-119">要取代的參數會以方括弧（...）括住， \[ \] 而且可能是屬性、環境變數 (% prefix) 、檔案路徑 (\# 首碼) 或元件目錄路徑 ($ prefix) 。</span><span class="sxs-lookup"><span data-stu-id="6e700-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="6e700-120">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="6e700-120">Return Processing Options</span></span>

<span data-ttu-id="6e700-121">自訂動作不會使用這些選項。</span><span class="sxs-lookup"><span data-stu-id="6e700-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="6e700-122">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="6e700-122">Execution Scheduling Options</span></span>

<span data-ttu-id="6e700-123">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="6e700-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="6e700-124">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="6e700-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="6e700-125">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="6e700-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="6e700-126">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="6e700-126">In-Script Execution Options</span></span>

<span data-ttu-id="6e700-127">自訂動作不會使用這些選項。</span><span class="sxs-lookup"><span data-stu-id="6e700-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="6e700-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e700-128">Return Values</span></span>

<span data-ttu-id="6e700-129">請參閱 [自訂動作傳回值](custom-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6e700-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e700-130">備註</span><span class="sxs-lookup"><span data-stu-id="6e700-130">Remarks</span></span>

<span data-ttu-id="6e700-131">如果您在 UI 序列中，藉由在其中一個使用者介面順序資料表中撰寫自訂動作來設定 [私用屬性](private-properties.md) ，該屬性就不會在執行順序中設定。</span><span class="sxs-lookup"><span data-stu-id="6e700-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="6e700-132">若要在執行順序中設定屬性，您也必須在執行順序資料表中放置自訂動作。</span><span class="sxs-lookup"><span data-stu-id="6e700-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="6e700-133">或者，您可以將屬性設為 [公用屬性](public-properties.md) ，並將它包含在 [**SecureCustomProperties 屬性**](securecustomproperties.md)中。</span><span class="sxs-lookup"><span data-stu-id="6e700-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e700-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e700-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e700-135">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="6e700-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6e700-136">格式化的文本自訂動作</span><span class="sxs-lookup"><span data-stu-id="6e700-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



