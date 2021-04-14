---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型54。
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: 自訂動作類型54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469332"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="9cc31-103">自訂動作類型54</span><span class="sxs-lookup"><span data-stu-id="9cc31-103">Custom Action Type 54</span></span>

<span data-ttu-id="9cc31-104">此自訂動作是以 VBScript 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="9cc31-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="9cc31-105">另請參閱 [腳本](scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc31-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="9cc31-106">來源</span><span class="sxs-lookup"><span data-stu-id="9cc31-106">Source</span></span>

<span data-ttu-id="9cc31-107">[CustomAction 資料表](customaction-table.md)的 [來源] 欄位包含屬性名稱，或是包含腳本文字之屬性的[屬性工作表](property-table.md)索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9cc31-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="9cc31-108">類型值</span><span class="sxs-lookup"><span data-stu-id="9cc31-108">Type Value</span></span>

<span data-ttu-id="9cc31-109">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="9cc31-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="9cc31-110">常數</span><span class="sxs-lookup"><span data-stu-id="9cc31-110">Constants</span></span>                                                             | <span data-ttu-id="9cc31-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="9cc31-111">Hexadecimal</span></span> | <span data-ttu-id="9cc31-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="9cc31-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9cc31-113">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="9cc31-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="9cc31-114">0x036</span><span class="sxs-lookup"><span data-stu-id="9cc31-114">0x036</span></span>       | <span data-ttu-id="9cc31-115">54</span><span class="sxs-lookup"><span data-stu-id="9cc31-115">54</span></span>      |



 

<span data-ttu-id="9cc31-116">Windows Installer 可以在64位作業系統上使用64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9cc31-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="9cc31-117">以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。</span><span class="sxs-lookup"><span data-stu-id="9cc31-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="9cc31-118">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc31-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="9cc31-119">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="9cc31-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="9cc31-120">常數</span><span class="sxs-lookup"><span data-stu-id="9cc31-120">Constants</span></span>                                                                                                    | <span data-ttu-id="9cc31-121">十六進位</span><span class="sxs-lookup"><span data-stu-id="9cc31-121">Hexadecimal</span></span> | <span data-ttu-id="9cc31-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="9cc31-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9cc31-123">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeProperty**  + **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9cc31-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9cc31-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="9cc31-124">0x0001036</span></span>   | <span data-ttu-id="9cc31-125">4150</span><span class="sxs-lookup"><span data-stu-id="9cc31-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="9cc31-126">目標</span><span class="sxs-lookup"><span data-stu-id="9cc31-126">Target</span></span>

<span data-ttu-id="9cc31-127">[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="9cc31-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="9cc31-128">處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="9cc31-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9cc31-129">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="9cc31-129">Return Processing Options</span></span>

<span data-ttu-id="9cc31-130">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="9cc31-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9cc31-131">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc31-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9cc31-132">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="9cc31-132">Execution Scheduling Options</span></span>

<span data-ttu-id="9cc31-133">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="9cc31-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9cc31-134">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="9cc31-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9cc31-135">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc31-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9cc31-136">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="9cc31-136">In-Script Execution Options</span></span>

<span data-ttu-id="9cc31-137">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="9cc31-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9cc31-138">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="9cc31-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9cc31-139">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc31-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9cc31-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cc31-140">Return Values</span></span>

<span data-ttu-id="9cc31-141">以腳本撰寫的選擇性函式必須傳回 [JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9cc31-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc31-142">備註</span><span class="sxs-lookup"><span data-stu-id="9cc31-142">Remarks</span></span>

<span data-ttu-id="9cc31-143">以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話**](session-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9cc31-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="9cc31-144">安裝程式會使用名稱 *會話* 將 **會話物件** 附加至腳本。</span><span class="sxs-lookup"><span data-stu-id="9cc31-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="9cc31-145">因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。</span><span class="sxs-lookup"><span data-stu-id="9cc31-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cc31-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cc31-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc31-147">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="9cc31-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



