---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型17。
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: 自訂動作類型17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320576"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="9ce58-103">自訂動作類型17</span><span class="sxs-lookup"><span data-stu-id="9ce58-103">Custom Action Type 17</span></span>

<span data-ttu-id="9ce58-104">此自訂動作會呼叫以 C 或 c + + 撰寫的動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="9ce58-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="9ce58-105">來源</span><span class="sxs-lookup"><span data-stu-id="9ce58-105">Source</span></span>

<span data-ttu-id="9ce58-106">DLL 會在目前的會話期間與應用程式一起安裝。</span><span class="sxs-lookup"><span data-stu-id="9ce58-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="9ce58-107">[CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9ce58-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="9ce58-108">自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，在安裝該檔案之後，以及移除之前，必須呼叫這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9ce58-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="9ce58-109">類型值</span><span class="sxs-lookup"><span data-stu-id="9ce58-109">Type Value</span></span>

<span data-ttu-id="9ce58-110">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="9ce58-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="9ce58-111">常數</span><span class="sxs-lookup"><span data-stu-id="9ce58-111">Constants</span></span>                                                          | <span data-ttu-id="9ce58-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="9ce58-112">Hexadecimal</span></span> | <span data-ttu-id="9ce58-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="9ce58-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9ce58-114">**msidbCustomActionTypeDll**  + **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="9ce58-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="9ce58-115">0x011</span><span class="sxs-lookup"><span data-stu-id="9ce58-115">0x011</span></span>       | <span data-ttu-id="9ce58-116">17</span><span class="sxs-lookup"><span data-stu-id="9ce58-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="9ce58-117">目標</span><span class="sxs-lookup"><span data-stu-id="9ce58-117">Target</span></span>

<span data-ttu-id="9ce58-118">DLL 是透過 [CustomAction 資料表](customaction-table.md)的目標欄位中名為的進入點來呼叫，並傳遞做為目前安裝會話控制碼的單一引數。</span><span class="sxs-lookup"><span data-stu-id="9ce58-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="9ce58-119">資料表中指定的進入點名稱必須符合從 DLL 匯出的專案點名稱。</span><span class="sxs-lookup"><span data-stu-id="9ce58-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="9ce58-120">請注意，如果未指定專案函數，則為。DEF 檔案或/EXPORT：連結器規格，名稱可能會有前置底線和 " @4 " 尾碼。</span><span class="sxs-lookup"><span data-stu-id="9ce58-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="9ce58-121">呼叫的函式必須指定 \_ \_ stdcall 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="9ce58-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9ce58-122">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="9ce58-122">Return Processing Options</span></span>

<span data-ttu-id="9ce58-123">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。</span><span class="sxs-lookup"><span data-stu-id="9ce58-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9ce58-124">如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce58-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9ce58-125">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="9ce58-125">Execution Scheduling Options</span></span>

<span data-ttu-id="9ce58-126">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="9ce58-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9ce58-127">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="9ce58-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9ce58-128">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce58-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9ce58-129">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="9ce58-129">In-Script Execution Options</span></span>

<span data-ttu-id="9ce58-130">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。</span><span class="sxs-lookup"><span data-stu-id="9ce58-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9ce58-131">這些選項會將動作程式碼複製到執行、復原或認可腳本中。</span><span class="sxs-lookup"><span data-stu-id="9ce58-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9ce58-132">如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce58-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9ce58-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ce58-133">Return Values</span></span>

<span data-ttu-id="9ce58-134">請參閱 [自訂動作傳回值](custom-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce58-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ce58-135">備註</span><span class="sxs-lookup"><span data-stu-id="9ce58-135">Remarks</span></span>

<span data-ttu-id="9ce58-136">呼叫動態連結程式庫 (DLL) 的自訂動作需要安裝會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9ce58-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="9ce58-137">如果這也是延後執行自訂動作，則在執行安裝腳本時，會話可能不再存在。</span><span class="sxs-lookup"><span data-stu-id="9ce58-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="9ce58-138">如需此類型的自訂動作如何取得內容資訊的相關資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce58-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="9ce58-139">自訂動作會在不同的執行緒中執行，而且可能會對系統有有限的存取權。</span><span class="sxs-lookup"><span data-stu-id="9ce58-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="9ce58-140">以非同步方式執行的自訂動作會在目前序列或安裝會話終止時封鎖主執行緒，直到它們傳回為止。</span><span class="sxs-lookup"><span data-stu-id="9ce58-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="9ce58-141">參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 17 (DLL) ）必須遵守下列排序限制：</span><span class="sxs-lookup"><span data-stu-id="9ce58-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="9ce58-142">自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="9ce58-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="9ce58-143">這是為了讓自訂動作能夠解析尋找 DLL 所需的路徑。</span><span class="sxs-lookup"><span data-stu-id="9ce58-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="9ce58-144">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9ce58-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="9ce58-145">如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9ce58-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ce58-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ce58-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ce58-147">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="9ce58-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="9ce58-148">延後執行自訂動作</span><span class="sxs-lookup"><span data-stu-id="9ce58-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="9ce58-149">動態連結程式庫</span><span class="sxs-lookup"><span data-stu-id="9ce58-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



