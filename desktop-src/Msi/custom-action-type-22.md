---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型22。
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: 自訂動作類型22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321228"
---
# <a name="custom-action-type-22"></a><span data-ttu-id="a309c-103">自訂動作類型22</span><span class="sxs-lookup"><span data-stu-id="a309c-103">Custom Action Type 22</span></span>

<span data-ttu-id="a309c-104">此自訂動作是以 VBScript 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="a309c-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="a309c-105">另請參閱 [腳本](scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="a309c-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="a309c-106">來源</span><span class="sxs-lookup"><span data-stu-id="a309c-106">Source</span></span>

<span data-ttu-id="a309c-107">腳本會在目前的會話期間與應用程式一起安裝。</span><span class="sxs-lookup"><span data-stu-id="a309c-107">The script is installed with the application during the current session.</span></span> <span data-ttu-id="a309c-108">[CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a309c-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="a309c-109">自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，必須在安裝檔案之後以及移除之前呼叫這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a309c-109">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="a309c-110">類型值</span><span class="sxs-lookup"><span data-stu-id="a309c-110">Type Value</span></span>

<span data-ttu-id="a309c-111">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="a309c-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="a309c-112">常數</span><span class="sxs-lookup"><span data-stu-id="a309c-112">Constants</span></span>                                                               | <span data-ttu-id="a309c-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="a309c-113">Hexadecimal</span></span> | <span data-ttu-id="a309c-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="a309c-114">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a309c-115">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="a309c-115">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="a309c-116">0x016</span><span class="sxs-lookup"><span data-stu-id="a309c-116">0x016</span></span>       | <span data-ttu-id="a309c-117">22</span><span class="sxs-lookup"><span data-stu-id="a309c-117">22</span></span>      |



 

<span data-ttu-id="a309c-118">Windows Installer 可以在64位作業系統上使用64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a309c-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="a309c-119">以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。</span><span class="sxs-lookup"><span data-stu-id="a309c-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="a309c-120">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="a309c-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="a309c-121">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="a309c-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="a309c-122">常數</span><span class="sxs-lookup"><span data-stu-id="a309c-122">Constants</span></span>                                                                                                      | <span data-ttu-id="a309c-123">十六進位</span><span class="sxs-lookup"><span data-stu-id="a309c-123">Hexadecimal</span></span> | <span data-ttu-id="a309c-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="a309c-124">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a309c-125">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeSourceFile**  + **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="a309c-125">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="a309c-126">0x0001016</span><span class="sxs-lookup"><span data-stu-id="a309c-126">0x0001016</span></span>   | <span data-ttu-id="a309c-127">4118</span><span class="sxs-lookup"><span data-stu-id="a309c-127">4118</span></span>    |



 

## <a name="target"></a><span data-ttu-id="a309c-128">目標</span><span class="sxs-lookup"><span data-stu-id="a309c-128">Target</span></span>

<span data-ttu-id="a309c-129">[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="a309c-129">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="a309c-130">處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="a309c-130">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a309c-131">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="a309c-131">Return Processing Options</span></span>

<span data-ttu-id="a309c-132">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="a309c-132">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="a309c-133">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="a309c-133">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a309c-134">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="a309c-134">Execution Scheduling Options</span></span>

<span data-ttu-id="a309c-135">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="a309c-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="a309c-136">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="a309c-136">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a309c-137">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="a309c-137">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a309c-138">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="a309c-138">In-Script Execution Options</span></span>

<span data-ttu-id="a309c-139">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="a309c-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="a309c-140">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="a309c-140">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="a309c-141">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="a309c-141">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="a309c-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="a309c-142">Return Values</span></span>

<span data-ttu-id="a309c-143">以腳本撰寫的選擇性函式必須傳回 [JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a309c-143">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a309c-144">備註</span><span class="sxs-lookup"><span data-stu-id="a309c-144">Remarks</span></span>

<span data-ttu-id="a309c-145">以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話物件**](session-object.md)。</span><span class="sxs-lookup"><span data-stu-id="a309c-145">A custom action that is written in JScript or VBScript requires the install [**Session Object**](session-object.md).</span></span> <span data-ttu-id="a309c-146">這是 **Session 物件** 類型，而安裝程式會將它附加至名稱為 "Session" 的腳本。</span><span class="sxs-lookup"><span data-stu-id="a309c-146">This is of the type **Session Object** and the installer attaches it to the script with the name "Session".</span></span> <span data-ttu-id="a309c-147">因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。</span><span class="sxs-lookup"><span data-stu-id="a309c-147">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="a309c-148">參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 22 (VBcript) ）必須遵守下列排序限制：</span><span class="sxs-lookup"><span data-stu-id="a309c-148">Custom actions that reference an installed file as their source, such as Custom Action Type 22 (VBcript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="a309c-149">自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="a309c-149">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="a309c-150">如此一來，自訂動作就可以解析找出包含 VBScript 的原始程式檔所需的路徑。</span><span class="sxs-lookup"><span data-stu-id="a309c-150">This is so that the custom action can resolve the path needed to locate the source file containing the VBScript.</span></span>
-   <span data-ttu-id="a309c-151">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a309c-151">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="a309c-152">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a309c-152">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a309c-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="a309c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a309c-154">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="a309c-154">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



