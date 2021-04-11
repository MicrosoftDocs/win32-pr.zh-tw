---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型21。
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: 自訂動作類型21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320575"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="02f57-103">自訂動作類型21</span><span class="sxs-lookup"><span data-stu-id="02f57-103">Custom Action Type 21</span></span>

<span data-ttu-id="02f57-104">此自訂動作是以 JScript 撰寫，例如 ECMA 262。</span><span class="sxs-lookup"><span data-stu-id="02f57-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="02f57-105">Windows Installer 不支援 JScript 1.0。</span><span class="sxs-lookup"><span data-stu-id="02f57-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="02f57-106">如需詳細資訊，請參閱 [腳本](scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="02f57-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="02f57-107">來源</span><span class="sxs-lookup"><span data-stu-id="02f57-107">Source</span></span>

<span data-ttu-id="02f57-108">腳本會在目前的會話期間與應用程式一起安裝。</span><span class="sxs-lookup"><span data-stu-id="02f57-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="02f57-109">[CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="02f57-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="02f57-110">自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，必須在安裝檔案之後以及移除之前呼叫這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="02f57-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="02f57-111">類型值</span><span class="sxs-lookup"><span data-stu-id="02f57-111">Type Value</span></span>

<span data-ttu-id="02f57-112">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="02f57-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="02f57-113">常數</span><span class="sxs-lookup"><span data-stu-id="02f57-113">Constants</span></span>                                                              | <span data-ttu-id="02f57-114">十六進位</span><span class="sxs-lookup"><span data-stu-id="02f57-114">Hexadecimal</span></span> | <span data-ttu-id="02f57-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="02f57-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="02f57-116">**msidbCustomActionTypeJScript**  + **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="02f57-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="02f57-117">0x015</span><span class="sxs-lookup"><span data-stu-id="02f57-117">0x015</span></span>       | <span data-ttu-id="02f57-118">21</span><span class="sxs-lookup"><span data-stu-id="02f57-118">21</span></span>      |



 

<span data-ttu-id="02f57-119">Windows Installer 可以在64位作業系統上使用 [64 位自訂動作](64-bit-custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="02f57-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="02f57-120">以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。</span><span class="sxs-lookup"><span data-stu-id="02f57-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="02f57-121">如需詳細資訊，請參閱64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="02f57-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="02f57-122">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="02f57-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="02f57-123">常數</span><span class="sxs-lookup"><span data-stu-id="02f57-123">Constants</span></span>                                                                                                     | <span data-ttu-id="02f57-124">十六進位</span><span class="sxs-lookup"><span data-stu-id="02f57-124">Hexadecimal</span></span> | <span data-ttu-id="02f57-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="02f57-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="02f57-126">**msidbCustomActionTypeJScript**  + **msidbCustomActionTypeSourceFile**  + **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="02f57-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="02f57-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="02f57-127">0x0001015</span></span>   | <span data-ttu-id="02f57-128">4117</span><span class="sxs-lookup"><span data-stu-id="02f57-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="02f57-129">目標</span><span class="sxs-lookup"><span data-stu-id="02f57-129">Target</span></span>

<span data-ttu-id="02f57-130">[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="02f57-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="02f57-131">處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="02f57-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="02f57-132">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="02f57-132">Return Processing Options</span></span>

<span data-ttu-id="02f57-133">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="02f57-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="02f57-134">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02f57-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="02f57-135">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="02f57-135">Execution Scheduling Options</span></span>

<span data-ttu-id="02f57-136">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="02f57-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="02f57-137">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="02f57-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="02f57-138">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02f57-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="02f57-139">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="02f57-139">In-Script Execution Options</span></span>

<span data-ttu-id="02f57-140">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="02f57-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="02f57-141">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="02f57-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="02f57-142">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02f57-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="02f57-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="02f57-143">Return Values</span></span>

<span data-ttu-id="02f57-144">以腳本撰寫的選擇性函式必須傳回 [JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="02f57-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02f57-145">備註</span><span class="sxs-lookup"><span data-stu-id="02f57-145">Remarks</span></span>

<span data-ttu-id="02f57-146">以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話**](session-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="02f57-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="02f57-147">安裝程式會將 **會話物件** 附加至名稱為 "Session" 的腳本。</span><span class="sxs-lookup"><span data-stu-id="02f57-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="02f57-148">因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。</span><span class="sxs-lookup"><span data-stu-id="02f57-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="02f57-149">參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 21 (JScript) ）必須遵守下列排序限制：</span><span class="sxs-lookup"><span data-stu-id="02f57-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="02f57-150">自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="02f57-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="02f57-151">這是為了讓自訂動作能夠解析找出包含 JScript 的原始程式檔所需的路徑。</span><span class="sxs-lookup"><span data-stu-id="02f57-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="02f57-152">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="02f57-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="02f57-153">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。</span><span class="sxs-lookup"><span data-stu-id="02f57-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02f57-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="02f57-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f57-155">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="02f57-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



