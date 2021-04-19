---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型6。
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: 自訂動作類型6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994375"
---
# <a name="custom-action-type-6"></a><span data-ttu-id="9b8cd-103">自訂動作類型6</span><span class="sxs-lookup"><span data-stu-id="9b8cd-103">Custom Action Type 6</span></span>

<span data-ttu-id="9b8cd-104">此自訂動作是以 VBScript 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="9b8cd-105">如需詳細資訊，請參閱 [腳本](scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-105">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="9b8cd-106">來源</span><span class="sxs-lookup"><span data-stu-id="9b8cd-106">Source</span></span>

<span data-ttu-id="9b8cd-107">腳本是從暫時性二進位資料流程產生的。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-107">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="9b8cd-108">[CustomAction 資料表](customaction-table.md)的來源欄位包含[二進位資料表](binary-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="9b8cd-109">二進位資料表中的資料行包含資料流程資料。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-109">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="9b8cd-110">針對每個資料列配置個別的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-110">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="9b8cd-111">您可以使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ，然後使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入資料表中，以從檔案插入新的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-111">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="9b8cd-112">叫用自訂動作時，資料流程資料會複製到暫存檔，然後根據自訂動作的類型進行處理。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-112">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="9b8cd-113">類型值</span><span class="sxs-lookup"><span data-stu-id="9b8cd-113">Type Value</span></span>

<span data-ttu-id="9b8cd-114">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-114">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="9b8cd-115">常數</span><span class="sxs-lookup"><span data-stu-id="9b8cd-115">Constants</span></span>                                                               | <span data-ttu-id="9b8cd-116">十六進位</span><span class="sxs-lookup"><span data-stu-id="9b8cd-116">Hexadecimal</span></span> | <span data-ttu-id="9b8cd-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="9b8cd-117">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9b8cd-118">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="9b8cd-118">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="9b8cd-119">0x006</span><span class="sxs-lookup"><span data-stu-id="9b8cd-119">0x006</span></span>       | <span data-ttu-id="9b8cd-120">6</span><span class="sxs-lookup"><span data-stu-id="9b8cd-120">6</span></span>       |



 

<span data-ttu-id="9b8cd-121">Windows Installer 可以在64位作業系統上使用64位自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-121">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="9b8cd-122">以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-122">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="9b8cd-123">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-123">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="9b8cd-124">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-124">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="9b8cd-125">常數</span><span class="sxs-lookup"><span data-stu-id="9b8cd-125">Constants</span></span>                                                                                                      | <span data-ttu-id="9b8cd-126">十六進位</span><span class="sxs-lookup"><span data-stu-id="9b8cd-126">Hexadecimal</span></span> | <span data-ttu-id="9b8cd-127">Decimal</span><span class="sxs-lookup"><span data-stu-id="9b8cd-127">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9b8cd-128">**msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeBinaryData**  + **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9b8cd-128">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9b8cd-129">0x0001006</span><span class="sxs-lookup"><span data-stu-id="9b8cd-129">0x0001006</span></span>   | <span data-ttu-id="9b8cd-130">4102</span><span class="sxs-lookup"><span data-stu-id="9b8cd-130">4102</span></span>    |



 

## <a name="target"></a><span data-ttu-id="9b8cd-131">目標</span><span class="sxs-lookup"><span data-stu-id="9b8cd-131">Target</span></span>

<span data-ttu-id="9b8cd-132">[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-132">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="9b8cd-133">處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-133">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9b8cd-134">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="9b8cd-134">Return Processing Options</span></span>

<span data-ttu-id="9b8cd-135">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9b8cd-136">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-136">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9b8cd-137">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="9b8cd-137">Execution Scheduling Options</span></span>

<span data-ttu-id="9b8cd-138">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9b8cd-139">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-139">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9b8cd-140">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-140">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9b8cd-141">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="9b8cd-141">In-Script Execution Options</span></span>

<span data-ttu-id="9b8cd-142">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-142">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9b8cd-143">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-143">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9b8cd-144">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-144">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9b8cd-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b8cd-145">Return Values</span></span>

<span data-ttu-id="9b8cd-146">以腳本撰寫的選擇性函式必須傳回 [JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-146">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b8cd-147">備註</span><span class="sxs-lookup"><span data-stu-id="9b8cd-147">Remarks</span></span>

<span data-ttu-id="9b8cd-148">以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話物件**](session-object.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-148">A custom action that is written in JScript or VBScript requires the installation of the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="9b8cd-149">安裝程式會使用名稱 *會話* 將 **會話** 物件附加至腳本。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-149">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="9b8cd-150">因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-150">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="9b8cd-151">匯出資料庫資料表時，會將每個資料流程寫入至資料表所命名之子資料夾中的個別檔案，並使用主鍵作為二進位資料表) 的檔案名 (名稱資料行，且預設副檔名為 "ibd"。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-151">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="9b8cd-152">如果檔案系統或版本控制系統不支援長檔名，則名稱應該使用8.3 檔案名格式。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-152">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="9b8cd-153">持續性封存檔案會以使用的檔案名取代資料流程資料，讓您可以在匯入資料表時找出資料。</span><span class="sxs-lookup"><span data-stu-id="9b8cd-153">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b8cd-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b8cd-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b8cd-155">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="9b8cd-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



