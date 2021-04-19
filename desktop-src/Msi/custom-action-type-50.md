---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型50。
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: 自訂動作類型50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994432"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="7907d-103">自訂動作類型50</span><span class="sxs-lookup"><span data-stu-id="7907d-103">Custom Action Type 50</span></span>

<span data-ttu-id="7907d-104">此自訂動作會呼叫使用命令列啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="7907d-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="7907d-105">另請參閱 [可執行檔](executable-files.md)。</span><span class="sxs-lookup"><span data-stu-id="7907d-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="7907d-106">來源</span><span class="sxs-lookup"><span data-stu-id="7907d-106">Source</span></span>

<span data-ttu-id="7907d-107">可執行檔是從現有的檔案產生的。</span><span class="sxs-lookup"><span data-stu-id="7907d-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="7907d-108">[CustomAction 資料表](customaction-table.md)的 [來源] 欄位包含屬性[表](property-table.md)的索引鍵，其中包含可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7907d-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="7907d-109">類型值</span><span class="sxs-lookup"><span data-stu-id="7907d-109">Type Value</span></span>

<span data-ttu-id="7907d-110">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="7907d-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="7907d-111">常數</span><span class="sxs-lookup"><span data-stu-id="7907d-111">Constants</span></span>                                                        | <span data-ttu-id="7907d-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="7907d-112">Hexadecimal</span></span> | <span data-ttu-id="7907d-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="7907d-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="7907d-114">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="7907d-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="7907d-115">0x032</span><span class="sxs-lookup"><span data-stu-id="7907d-115">0x032</span></span>       | <span data-ttu-id="7907d-116">50</span><span class="sxs-lookup"><span data-stu-id="7907d-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="7907d-117">目標</span><span class="sxs-lookup"><span data-stu-id="7907d-117">Target</span></span>

<span data-ttu-id="7907d-118">[CustomAction 資料表](customaction-table.md)的目標資料行包含在來源資料行中所識別之可執行檔的命令列字串。</span><span class="sxs-lookup"><span data-stu-id="7907d-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7907d-119">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="7907d-119">Return Processing Options</span></span>

<span data-ttu-id="7907d-120">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="7907d-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="7907d-121">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="7907d-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7907d-122">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="7907d-122">Execution Scheduling Options</span></span>

<span data-ttu-id="7907d-123">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="7907d-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="7907d-124">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="7907d-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="7907d-125">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="7907d-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7907d-126">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="7907d-126">In-Script Execution Options</span></span>

<span data-ttu-id="7907d-127">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="7907d-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="7907d-128">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="7907d-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="7907d-129">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="7907d-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="7907d-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="7907d-130">Return Values</span></span>

<span data-ttu-id="7907d-131">[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。</span><span class="sxs-lookup"><span data-stu-id="7907d-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="7907d-132">安裝程式會將任何其他傳回值視為失敗。</span><span class="sxs-lookup"><span data-stu-id="7907d-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="7907d-133">若要忽略傳回值，請在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="7907d-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="7907d-134">備註</span><span class="sxs-lookup"><span data-stu-id="7907d-134">Remarks</span></span>

<span data-ttu-id="7907d-135">啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="7907d-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="7907d-136">如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 CreateProcessAsUser 或 CreateProcess 來建立進程。</span><span class="sxs-lookup"><span data-stu-id="7907d-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7907d-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="7907d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7907d-138">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="7907d-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



