---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型2。
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: 自訂動作類型2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984222"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="db967-103">自訂動作類型2</span><span class="sxs-lookup"><span data-stu-id="db967-103">Custom Action Type 2</span></span>

<span data-ttu-id="db967-104">此自訂動作會呼叫使用命令列啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="db967-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="db967-105">來源</span><span class="sxs-lookup"><span data-stu-id="db967-105">Source</span></span>

<span data-ttu-id="db967-106">可執行檔是從暫時二進位資料流程產生的。</span><span class="sxs-lookup"><span data-stu-id="db967-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="db967-107">[CustomAction 資料表](customaction-table.md)的來源欄位包含[二進位資料表](binary-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="db967-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="db967-108">二進位資料表中的資料行包含資料流程資料。</span><span class="sxs-lookup"><span data-stu-id="db967-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="db967-109">針對每個資料列配置個別的資料流程。</span><span class="sxs-lookup"><span data-stu-id="db967-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="db967-110">您可以使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ，然後使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入資料表中，以從檔案插入新的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="db967-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="db967-111">叫用自訂動作時，資料流程資料會複製到暫存檔，然後根據自訂動作的類型進行處理。</span><span class="sxs-lookup"><span data-stu-id="db967-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="db967-112">類型值</span><span class="sxs-lookup"><span data-stu-id="db967-112">Type Value</span></span>

<span data-ttu-id="db967-113">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="db967-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="db967-114">常數</span><span class="sxs-lookup"><span data-stu-id="db967-114">Constants</span></span>                                                          | <span data-ttu-id="db967-115">十六進位</span><span class="sxs-lookup"><span data-stu-id="db967-115">Hexadecimal</span></span> | <span data-ttu-id="db967-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="db967-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="db967-117">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="db967-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="db967-118">0x002</span><span class="sxs-lookup"><span data-stu-id="db967-118">0x002</span></span>       | <span data-ttu-id="db967-119">2</span><span class="sxs-lookup"><span data-stu-id="db967-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="db967-120">目標</span><span class="sxs-lookup"><span data-stu-id="db967-120">Target</span></span>

<span data-ttu-id="db967-121">[CustomAction 資料表](customaction-table.md)的目標資料行包含來源資料行中所指定之可執行檔的命令列字串。</span><span class="sxs-lookup"><span data-stu-id="db967-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="db967-122">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="db967-122">Return Processing Options</span></span>

<span data-ttu-id="db967-123">在 CustomAction 資料表的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="db967-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="db967-124">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="db967-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="db967-125">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="db967-125">Execution Scheduling Options</span></span>

<span data-ttu-id="db967-126">在 CustomAction 資料表的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="db967-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="db967-127">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="db967-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="db967-128">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="db967-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="db967-129">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="db967-129">In-Script Execution Options</span></span>

<span data-ttu-id="db967-130">在 CustomAction 資料表的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="db967-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="db967-131">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="db967-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="db967-132">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="db967-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="db967-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="db967-133">Return Values</span></span>

<span data-ttu-id="db967-134">[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。</span><span class="sxs-lookup"><span data-stu-id="db967-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="db967-135">安裝程式會將任何其他傳回值視為失敗。</span><span class="sxs-lookup"><span data-stu-id="db967-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="db967-136">若要忽略傳回值，請在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="db967-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="db967-137">備註</span><span class="sxs-lookup"><span data-stu-id="db967-137">Remarks</span></span>

<span data-ttu-id="db967-138">啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="db967-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="db967-139">如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 來建立進程。</span><span class="sxs-lookup"><span data-stu-id="db967-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="db967-140">匯出資料庫資料表時，會將每個資料流程寫入至資料表所命名之子資料夾中的個別檔案，並使用主鍵作為二進位資料表) 的檔案名 (名稱資料行，且預設副檔名為 "ibd"。</span><span class="sxs-lookup"><span data-stu-id="db967-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="db967-141">如果檔案系統或版本控制系統不支援長檔名，則名稱應該使用8.3 格式。</span><span class="sxs-lookup"><span data-stu-id="db967-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="db967-142">持續性封存檔案會以使用的檔案名取代資料流程資料，讓您可以在匯入資料表時找出資料。</span><span class="sxs-lookup"><span data-stu-id="db967-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db967-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="db967-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db967-144">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="db967-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="db967-145">可執行檔</span><span class="sxs-lookup"><span data-stu-id="db967-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
