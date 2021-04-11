---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型38。
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: 自訂動作類型38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944762"
---
# <a name="custom-action-type-38"></a><span data-ttu-id="607c6-103">自訂動作類型38</span><span class="sxs-lookup"><span data-stu-id="607c6-103">Custom Action Type 38</span></span>

<span data-ttu-id="607c6-104">此自訂動作是以 VBScript 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="607c6-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="607c6-105">另請參閱 [腳本](scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="607c6-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="607c6-106">來源</span><span class="sxs-lookup"><span data-stu-id="607c6-106">Source</span></span>

<span data-ttu-id="607c6-107">[CustomAction 資料表](customaction-table.md)的來源欄位包含 null 值。</span><span class="sxs-lookup"><span data-stu-id="607c6-107">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="607c6-108">自訂動作的腳本程式碼會以常值腳本文字的字串儲存在目標欄位中。</span><span class="sxs-lookup"><span data-stu-id="607c6-108">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="607c6-109">類型值</span><span class="sxs-lookup"><span data-stu-id="607c6-109">Type Value</span></span>

<span data-ttu-id="607c6-110">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="607c6-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="607c6-111">常數</span><span class="sxs-lookup"><span data-stu-id="607c6-111">Constants</span></span>                                                              | <span data-ttu-id="607c6-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="607c6-112">Hexadecimal</span></span> | <span data-ttu-id="607c6-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="607c6-113">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="607c6-114">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="607c6-114">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="607c6-115">0x026</span><span class="sxs-lookup"><span data-stu-id="607c6-115">0x026</span></span>       | <span data-ttu-id="607c6-116">38</span><span class="sxs-lookup"><span data-stu-id="607c6-116">38</span></span>      |



 

<span data-ttu-id="607c6-117">Windows Installer 可以在64位作業系統上使用64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="607c6-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="607c6-118">以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。</span><span class="sxs-lookup"><span data-stu-id="607c6-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="607c6-119">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="607c6-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="607c6-120">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="607c6-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="607c6-121">常數</span><span class="sxs-lookup"><span data-stu-id="607c6-121">Constants</span></span>                                                                                                     | <span data-ttu-id="607c6-122">十六進位</span><span class="sxs-lookup"><span data-stu-id="607c6-122">Hexadecimal</span></span> | <span data-ttu-id="607c6-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="607c6-123">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="607c6-124">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeDirectory**  + **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="607c6-124">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="607c6-125">0x0001026</span><span class="sxs-lookup"><span data-stu-id="607c6-125">0x0001026</span></span>   | <span data-ttu-id="607c6-126">4134</span><span class="sxs-lookup"><span data-stu-id="607c6-126">4134</span></span>    |



 

## <a name="target"></a><span data-ttu-id="607c6-127">目標</span><span class="sxs-lookup"><span data-stu-id="607c6-127">Target</span></span>

<span data-ttu-id="607c6-128">[CustomAction 資料表](customaction-table.md)的 [目標] 欄位包含自訂動作的腳本程式碼，做為常值腳本文字的字串。</span><span class="sxs-lookup"><span data-stu-id="607c6-128">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="607c6-129">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="607c6-129">Return Processing Options</span></span>

<span data-ttu-id="607c6-130">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="607c6-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="607c6-131">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="607c6-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="607c6-132">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="607c6-132">Execution Scheduling Options</span></span>

<span data-ttu-id="607c6-133">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="607c6-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="607c6-134">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="607c6-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="607c6-135">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="607c6-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="607c6-136">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="607c6-136">In-Script Execution Options</span></span>

<span data-ttu-id="607c6-137">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="607c6-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="607c6-138">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="607c6-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="607c6-139">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="607c6-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="607c6-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="607c6-140">Return Values</span></span>

<span data-ttu-id="607c6-141">此自訂動作類型一律會傳回成功。</span><span class="sxs-lookup"><span data-stu-id="607c6-141">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="607c6-142">備註</span><span class="sxs-lookup"><span data-stu-id="607c6-142">Remarks</span></span>

<span data-ttu-id="607c6-143">以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話**](session-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="607c6-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="607c6-144">安裝程式會將 **會話物件** 附加至名稱為 "Session" 的腳本。</span><span class="sxs-lookup"><span data-stu-id="607c6-144">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="607c6-145">因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。</span><span class="sxs-lookup"><span data-stu-id="607c6-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="607c6-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="607c6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="607c6-147">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="607c6-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



