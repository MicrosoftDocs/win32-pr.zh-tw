---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型1。
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: 自訂動作類型1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027453"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="a6db8-103">自訂動作類型1</span><span class="sxs-lookup"><span data-stu-id="a6db8-103">Custom Action Type 1</span></span>

<span data-ttu-id="a6db8-104">此自訂動作會呼叫以 C 或 c + + 撰寫的動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="a6db8-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="a6db8-105">來源</span><span class="sxs-lookup"><span data-stu-id="a6db8-105">Source</span></span>

<span data-ttu-id="a6db8-106">DLL 是從暫存二進位資料流程產生的。</span><span class="sxs-lookup"><span data-stu-id="a6db8-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="a6db8-107">[CustomAction 資料表](customaction-table.md)的來源欄位包含[二進位資料表](binary-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a6db8-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="a6db8-108">二進位資料表中的資料行包含資料流程資料。</span><span class="sxs-lookup"><span data-stu-id="a6db8-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="a6db8-109">針對每個資料列配置個別的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a6db8-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="a6db8-110">您可以使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ，然後使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入資料表中，以從檔案插入新的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="a6db8-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="a6db8-111">叫用自訂動作時，資料流程資料會複製到暫存檔，然後根據自訂動作的類型進行處理。</span><span class="sxs-lookup"><span data-stu-id="a6db8-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="a6db8-112">類型值</span><span class="sxs-lookup"><span data-stu-id="a6db8-112">Type Value</span></span>

<span data-ttu-id="a6db8-113">在 [CustomAction 資料表](customaction-table.md) 的類型資料行中包含下列旗標位，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="a6db8-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="a6db8-114">常數</span><span class="sxs-lookup"><span data-stu-id="a6db8-114">Constants</span></span>                                                          | <span data-ttu-id="a6db8-115">十六進位</span><span class="sxs-lookup"><span data-stu-id="a6db8-115">Hexadecimal</span></span> | <span data-ttu-id="a6db8-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="a6db8-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a6db8-117">**msidbCustomActionTypeDll**  + **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="a6db8-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="a6db8-118">0x001</span><span class="sxs-lookup"><span data-stu-id="a6db8-118">0x001</span></span>       | <span data-ttu-id="a6db8-119">1</span><span class="sxs-lookup"><span data-stu-id="a6db8-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="a6db8-120">目標</span><span class="sxs-lookup"><span data-stu-id="a6db8-120">Target</span></span>

<span data-ttu-id="a6db8-121">DLL 是透過 [CustomAction 資料表](customaction-table.md)的目標欄位中名為的進入點來呼叫，並傳遞做為目前安裝會話控制碼的單一引數。</span><span class="sxs-lookup"><span data-stu-id="a6db8-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="a6db8-122">資料表中指定的進入點名稱必須符合從 DLL 匯出的專案點名稱。</span><span class="sxs-lookup"><span data-stu-id="a6db8-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="a6db8-123">請注意，如果未指定專案函數，則為。DEF 檔案或/EXPORT：連結器規格，名稱可能會有前置底線和 " @4 " 尾碼。</span><span class="sxs-lookup"><span data-stu-id="a6db8-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="a6db8-124">呼叫的函式必須指定 \_ \_ stdcall 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="a6db8-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a6db8-125">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="a6db8-125">Return Processing Options</span></span>

<span data-ttu-id="a6db8-126">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="a6db8-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="a6db8-127">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="a6db8-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a6db8-128">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="a6db8-128">Execution Scheduling Options</span></span>

<span data-ttu-id="a6db8-129">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="a6db8-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="a6db8-130">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="a6db8-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a6db8-131">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="a6db8-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a6db8-132">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="a6db8-132">In-Script Execution Options</span></span>

<span data-ttu-id="a6db8-133">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="a6db8-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="a6db8-134">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="a6db8-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="a6db8-135">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="a6db8-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="a6db8-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6db8-136">Return Values</span></span>

<span data-ttu-id="a6db8-137">請參閱 [自訂動作傳回值](custom-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="a6db8-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6db8-138">備註</span><span class="sxs-lookup"><span data-stu-id="a6db8-138">Remarks</span></span>

<span data-ttu-id="a6db8-139">呼叫動態連結程式庫 (DLL) 的自訂動作需要安裝會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6db8-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="a6db8-140">如果這也是延後執行自訂動作，則在執行安裝腳本時，會話可能不再存在。</span><span class="sxs-lookup"><span data-stu-id="a6db8-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="a6db8-141">如需此類型的自訂動作如何取得內容資訊的相關資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="a6db8-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="a6db8-142">匯出資料庫資料表時，會將每個資料流程寫入至資料表所命名之子資料夾中的個別檔案，並使用主鍵作為二進位資料表) 的檔案名 (名稱資料行，且預設副檔名為 "ibd"。</span><span class="sxs-lookup"><span data-stu-id="a6db8-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="a6db8-143">如果檔案系統或版本控制系統不支援長檔名，則名稱應該使用8.3 格式。</span><span class="sxs-lookup"><span data-stu-id="a6db8-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="a6db8-144">持續性封存檔案會以使用的檔案名取代資料流程資料，讓您可以在匯入資料表時找出資料。</span><span class="sxs-lookup"><span data-stu-id="a6db8-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6db8-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6db8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6db8-146">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="a6db8-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a6db8-147">動態連結程式庫</span><span class="sxs-lookup"><span data-stu-id="a6db8-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="a6db8-148">取得順延強制自訂動作的內容資訊</span><span class="sxs-lookup"><span data-stu-id="a6db8-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



