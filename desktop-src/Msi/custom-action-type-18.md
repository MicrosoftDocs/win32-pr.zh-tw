---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型18。
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: 自訂動作類型18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945208"
---
# <a name="custom-action-type-18"></a><span data-ttu-id="939b5-103">自訂動作類型18</span><span class="sxs-lookup"><span data-stu-id="939b5-103">Custom Action Type 18</span></span>

<span data-ttu-id="939b5-104">此自訂動作會呼叫使用命令列啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="939b5-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="939b5-105">來源</span><span class="sxs-lookup"><span data-stu-id="939b5-105">Source</span></span>

<span data-ttu-id="939b5-106">可執行檔是從隨應用程式安裝的檔案產生的。</span><span class="sxs-lookup"><span data-stu-id="939b5-106">The executable is generated from a file installed with the application.</span></span> <span data-ttu-id="939b5-107">[CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="939b5-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="939b5-108">自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，必須在安裝檔案之後以及移除之前呼叫這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="939b5-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="939b5-109">類型值</span><span class="sxs-lookup"><span data-stu-id="939b5-109">Type Value</span></span>

<span data-ttu-id="939b5-110">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="939b5-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="939b5-111">常數</span><span class="sxs-lookup"><span data-stu-id="939b5-111">Constants</span></span>                                                          | <span data-ttu-id="939b5-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="939b5-112">Hexadecimal</span></span> | <span data-ttu-id="939b5-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="939b5-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="939b5-114">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="939b5-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="939b5-115">0x012</span><span class="sxs-lookup"><span data-stu-id="939b5-115">0x012</span></span>       | <span data-ttu-id="939b5-116">18</span><span class="sxs-lookup"><span data-stu-id="939b5-116">18</span></span>      |



 

## <a name="target"></a><span data-ttu-id="939b5-117">目標</span><span class="sxs-lookup"><span data-stu-id="939b5-117">Target</span></span>

<span data-ttu-id="939b5-118">[CustomAction 資料表](customaction-table.md)的目標資料行包含在來源資料行中所識別之可執行檔的命令列字串。</span><span class="sxs-lookup"><span data-stu-id="939b5-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="939b5-119">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="939b5-119">Return Processing Options</span></span>

<span data-ttu-id="939b5-120">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="939b5-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="939b5-121">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="939b5-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="939b5-122">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="939b5-122">Execution Scheduling Options</span></span>

<span data-ttu-id="939b5-123">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="939b5-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="939b5-124">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="939b5-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="939b5-125">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="939b5-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="939b5-126">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="939b5-126">In-Script Execution Options</span></span>

<span data-ttu-id="939b5-127">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="939b5-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="939b5-128">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="939b5-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="939b5-129">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="939b5-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="939b5-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="939b5-130">Return Values</span></span>

<span data-ttu-id="939b5-131">[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。</span><span class="sxs-lookup"><span data-stu-id="939b5-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="939b5-132">安裝程式會將任何其他傳回值視為失敗。</span><span class="sxs-lookup"><span data-stu-id="939b5-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="939b5-133">若要忽略傳回值，請在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="939b5-133">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="939b5-134">備註</span><span class="sxs-lookup"><span data-stu-id="939b5-134">Remarks</span></span>

<span data-ttu-id="939b5-135">啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="939b5-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="939b5-136">如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 來建立進程。</span><span class="sxs-lookup"><span data-stu-id="939b5-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="939b5-137">參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 18 (EXE) ）必須遵守下列排序限制：</span><span class="sxs-lookup"><span data-stu-id="939b5-137">Custom actions that reference an installed file as their source, such as Custom Action Type 18 (EXE), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="939b5-138">自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="939b5-138">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="939b5-139">這是為了讓自訂動作能夠解析尋找 EXE 所需的路徑。</span><span class="sxs-lookup"><span data-stu-id="939b5-139">This is so that the custom action can resolve the path needed to locate the EXE.</span></span>
-   <span data-ttu-id="939b5-140">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="939b5-140">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="939b5-141">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。</span><span class="sxs-lookup"><span data-stu-id="939b5-141">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="939b5-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="939b5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="939b5-143">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="939b5-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="939b5-144">可執行檔</span><span class="sxs-lookup"><span data-stu-id="939b5-144">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
