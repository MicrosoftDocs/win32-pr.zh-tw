---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型53。
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: 自訂動作類型53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944562"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="2b97f-103">自訂動作類型53</span><span class="sxs-lookup"><span data-stu-id="2b97f-103">Custom Action Type 53</span></span>

<span data-ttu-id="2b97f-104">此自訂動作是以 JScript 撰寫，例如 ECMA 262。</span><span class="sxs-lookup"><span data-stu-id="2b97f-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="2b97f-105">Windows Installer 不支援 JScript 1.0。</span><span class="sxs-lookup"><span data-stu-id="2b97f-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="2b97f-106">如需詳細資訊，請參閱 [腳本](scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="2b97f-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="2b97f-107">來源</span><span class="sxs-lookup"><span data-stu-id="2b97f-107">Source</span></span>

<span data-ttu-id="2b97f-108">[CustomAction 資料表](customaction-table.md)的 [來源] 欄位包含屬性名稱，或是包含腳本文字之屬性的[屬性工作表](property-table.md)索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2b97f-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="2b97f-109">類型值</span><span class="sxs-lookup"><span data-stu-id="2b97f-109">Type Value</span></span>

<span data-ttu-id="2b97f-110">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="2b97f-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="2b97f-111">常數</span><span class="sxs-lookup"><span data-stu-id="2b97f-111">Constants</span></span>                                                            | <span data-ttu-id="2b97f-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="2b97f-112">Hexadecimal</span></span> | <span data-ttu-id="2b97f-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="2b97f-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="2b97f-114">**msidbCustomActionTypeJScript**  + **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="2b97f-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="2b97f-115">0x035</span><span class="sxs-lookup"><span data-stu-id="2b97f-115">0x035</span></span>       | <span data-ttu-id="2b97f-116">53</span><span class="sxs-lookup"><span data-stu-id="2b97f-116">53</span></span>      |



 

<span data-ttu-id="2b97f-117">Windows Installer 可以在64位作業系統上使用64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="2b97f-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="2b97f-118">以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。</span><span class="sxs-lookup"><span data-stu-id="2b97f-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="2b97f-119">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="2b97f-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="2b97f-120">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="2b97f-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="2b97f-121">常數</span><span class="sxs-lookup"><span data-stu-id="2b97f-121">Constants</span></span>                                                                                                   | <span data-ttu-id="2b97f-122">十六進位</span><span class="sxs-lookup"><span data-stu-id="2b97f-122">Hexadecimal</span></span> | <span data-ttu-id="2b97f-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="2b97f-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="2b97f-124">**msidbCustomActionTypeJScript**  + **msidbCustomActionTypeProperty**  + **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="2b97f-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="2b97f-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="2b97f-125">0x0001035</span></span>   | <span data-ttu-id="2b97f-126">4149</span><span class="sxs-lookup"><span data-stu-id="2b97f-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="2b97f-127">目標</span><span class="sxs-lookup"><span data-stu-id="2b97f-127">Target</span></span>

<span data-ttu-id="2b97f-128">[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="2b97f-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="2b97f-129">處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="2b97f-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="2b97f-130">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="2b97f-130">Return Processing Options</span></span>

<span data-ttu-id="2b97f-131">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="2b97f-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="2b97f-132">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="2b97f-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="2b97f-133">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="2b97f-133">Execution Scheduling Options</span></span>

<span data-ttu-id="2b97f-134">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="2b97f-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="2b97f-135">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="2b97f-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="2b97f-136">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="2b97f-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="2b97f-137">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="2b97f-137">In-Script Execution Options</span></span>

<span data-ttu-id="2b97f-138">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="2b97f-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="2b97f-139">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="2b97f-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="2b97f-140">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="2b97f-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="2b97f-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b97f-141">Return Values</span></span>

<span data-ttu-id="2b97f-142">以腳本撰寫的選擇性函式必須傳回 [JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2b97f-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b97f-143">備註</span><span class="sxs-lookup"><span data-stu-id="2b97f-143">Remarks</span></span>

<span data-ttu-id="2b97f-144">以 JScript 撰寫的自訂動作需要安裝 [**會話**](session-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2b97f-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="2b97f-145">因為 **會話** 物件在安裝復原期間可能不存在，所以以腳本撰寫的延遲自訂動作會使用 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)中所述的其中一個方法。</span><span class="sxs-lookup"><span data-stu-id="2b97f-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b97f-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b97f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b97f-147">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="2b97f-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



