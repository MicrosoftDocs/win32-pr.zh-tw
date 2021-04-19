---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型34。
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: 自訂動作類型34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997851"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="29978-103">自訂動作類型34</span><span class="sxs-lookup"><span data-stu-id="29978-103">Custom Action Type 34</span></span>

<span data-ttu-id="29978-104">此自訂動作會呼叫使用命令列啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="29978-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="29978-105">如需詳細資訊，請參閱 [可執行檔](executable-files.md)。</span><span class="sxs-lookup"><span data-stu-id="29978-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="29978-106">來源</span><span class="sxs-lookup"><span data-stu-id="29978-106">Source</span></span>

<span data-ttu-id="29978-107">可執行檔是從檔案產生的。</span><span class="sxs-lookup"><span data-stu-id="29978-107">The executable is generated from a file.</span></span> <span data-ttu-id="29978-108">[CustomAction](customaction-table.md)資料表的來源欄位包含[目錄](directory-table.md)資料表中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="29978-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="29978-109">參考的目錄資料表專案可用來解析工作目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="29978-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="29978-110">這不一定要是包含可執行檔之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="29978-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="29978-111">類型值</span><span class="sxs-lookup"><span data-stu-id="29978-111">Type Value</span></span>

<span data-ttu-id="29978-112">在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="29978-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="29978-113">常數</span><span class="sxs-lookup"><span data-stu-id="29978-113">Constants</span></span>                                                         | <span data-ttu-id="29978-114">十六進位</span><span class="sxs-lookup"><span data-stu-id="29978-114">Hexadecimal</span></span> | <span data-ttu-id="29978-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="29978-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="29978-116">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="29978-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="29978-117">0x022</span><span class="sxs-lookup"><span data-stu-id="29978-117">0x022</span></span>       | <span data-ttu-id="29978-118">34</span><span class="sxs-lookup"><span data-stu-id="29978-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="29978-119">目標</span><span class="sxs-lookup"><span data-stu-id="29978-119">Target</span></span>

<span data-ttu-id="29978-120">[CustomAction](customaction-table.md)資料表的目標資料行包含可執行檔的完整路徑和名稱，後面加上可執行檔的選擇性引數。</span><span class="sxs-lookup"><span data-stu-id="29978-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="29978-121">需要可執行檔的完整路徑和名稱。</span><span class="sxs-lookup"><span data-stu-id="29978-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="29978-122">引號必須用在長的檔案名或路徑周圍。</span><span class="sxs-lookup"><span data-stu-id="29978-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="29978-123">值會被視為 [格式化](formatted.md) 的文字，而且可能包含屬性、檔案、目錄或其他格式化文字屬性的參考。</span><span class="sxs-lookup"><span data-stu-id="29978-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="29978-124">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="29978-124">Return Processing Options</span></span>

<span data-ttu-id="29978-125">在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="29978-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="29978-126">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="29978-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="29978-127">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="29978-127">Execution Scheduling Options</span></span>

<span data-ttu-id="29978-128">在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="29978-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="29978-129">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="29978-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="29978-130">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="29978-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="29978-131">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="29978-131">In-Script Execution Options</span></span>

<span data-ttu-id="29978-132">在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="29978-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="29978-133">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="29978-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="29978-134">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="29978-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="29978-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="29978-135">Return Values</span></span>

<span data-ttu-id="29978-136">[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。</span><span class="sxs-lookup"><span data-stu-id="29978-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="29978-137">安裝程式會將任何其他傳回值視為失敗。</span><span class="sxs-lookup"><span data-stu-id="29978-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="29978-138">若要忽略傳回值，請在 [CustomAction](customaction-table.md)資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="29978-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="29978-139">備註</span><span class="sxs-lookup"><span data-stu-id="29978-139">Remarks</span></span>

<span data-ttu-id="29978-140">啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="29978-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="29978-141">如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 來建立進程。</span><span class="sxs-lookup"><span data-stu-id="29978-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29978-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="29978-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29978-143">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="29978-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
