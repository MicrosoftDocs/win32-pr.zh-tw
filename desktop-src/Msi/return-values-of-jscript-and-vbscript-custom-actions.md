---
description: 以 JScript 或 Visual Basic 撰寫的自訂動作、腳本版本 (VBScript) 可以呼叫選擇性的函式。 這些函數必須傳回下表所示的其中一個值。
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: JScript 和 VBScript 自訂動作的傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980752"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="84ac1-104">JScript 和 VBScript 自訂動作的傳回值</span><span class="sxs-lookup"><span data-stu-id="84ac1-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="84ac1-105">以 JScript 或 Visual Basic 撰寫的自訂動作、腳本版本 (VBScript) 可以呼叫選擇性的函式。</span><span class="sxs-lookup"><span data-stu-id="84ac1-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="84ac1-106">這些函數必須傳回下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="84ac1-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="84ac1-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="84ac1-107">Return value</span></span>              | <span data-ttu-id="84ac1-108">值</span><span class="sxs-lookup"><span data-stu-id="84ac1-108">Value</span></span>        | <span data-ttu-id="84ac1-109">描述</span><span class="sxs-lookup"><span data-stu-id="84ac1-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84ac1-110">msiDoActionStatusNoAction</span><span class="sxs-lookup"><span data-stu-id="84ac1-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="84ac1-111">0</span><span class="sxs-lookup"><span data-stu-id="84ac1-111">0</span></span>            | <span data-ttu-id="84ac1-112">未執行動作。</span><span class="sxs-lookup"><span data-stu-id="84ac1-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="84ac1-113">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="84ac1-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="84ac1-114">IDOK = 1</span><span class="sxs-lookup"><span data-stu-id="84ac1-114">IDOK = 1</span></span>     | <span data-ttu-id="84ac1-115">動作已成功完成。</span><span class="sxs-lookup"><span data-stu-id="84ac1-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="84ac1-116">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="84ac1-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="84ac1-117">IDCANCEL = 2</span><span class="sxs-lookup"><span data-stu-id="84ac1-117">IDCANCEL = 2</span></span> | <span data-ttu-id="84ac1-118">使用者提前終止。</span><span class="sxs-lookup"><span data-stu-id="84ac1-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="84ac1-119">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="84ac1-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="84ac1-120">IDABORT = 3</span><span class="sxs-lookup"><span data-stu-id="84ac1-120">IDABORT = 3</span></span>  | <span data-ttu-id="84ac1-121">無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="84ac1-121">Unrecoverable error.</span></span> <span data-ttu-id="84ac1-122">如果在剖析或執行 JScript 或 VBScript 期間發生錯誤，則傳回。</span><span class="sxs-lookup"><span data-stu-id="84ac1-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="84ac1-123">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="84ac1-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="84ac1-124">IDRETRY = 4</span><span class="sxs-lookup"><span data-stu-id="84ac1-124">IDRETRY = 4</span></span>  | <span data-ttu-id="84ac1-125">要在稍後繼續執行的暫止順序。</span><span class="sxs-lookup"><span data-stu-id="84ac1-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="84ac1-126">msiDoActionStatusFinished</span><span class="sxs-lookup"><span data-stu-id="84ac1-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="84ac1-127">IDIGNORE = 5</span><span class="sxs-lookup"><span data-stu-id="84ac1-127">IDIGNORE = 5</span></span> | <span data-ttu-id="84ac1-128">略過其餘的動作。</span><span class="sxs-lookup"><span data-stu-id="84ac1-128">Skip remaining actions.</span></span> <span data-ttu-id="84ac1-129">不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="84ac1-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="84ac1-130">請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。</span><span class="sxs-lookup"><span data-stu-id="84ac1-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="84ac1-131">例如，如果動作傳回值在記錄檔中顯示為 1 (一個) ，這表示該動作傳回 msiDoActionStatusSuccess。</span><span class="sxs-lookup"><span data-stu-id="84ac1-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="84ac1-132">如需此轉譯的詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="84ac1-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="84ac1-133">若要從腳本自訂動作傳回「成功」以外的值，您必須使用自訂動作的函數目標。</span><span class="sxs-lookup"><span data-stu-id="84ac1-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="84ac1-134">目標函數是在 [CustomAction 資料表](customaction-table.md)的目標資料行中指定。</span><span class="sxs-lookup"><span data-stu-id="84ac1-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="84ac1-135">下列腳本範例顯示如何從 VBScript 自訂動作傳回成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="84ac1-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="84ac1-136">如果這個 VBScript 內嵌在安裝套件的 [二進位資料表](binary-table.md) 中 MyCA.vbs，則腳本的 [CustomAction 資料表](customaction-table.md) 專案如下所示：</span><span class="sxs-lookup"><span data-stu-id="84ac1-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="84ac1-137">動作</span><span class="sxs-lookup"><span data-stu-id="84ac1-137">Action</span></span>         | <span data-ttu-id="84ac1-138">類型</span><span class="sxs-lookup"><span data-stu-id="84ac1-138">Type</span></span> | <span data-ttu-id="84ac1-139">來源</span><span class="sxs-lookup"><span data-stu-id="84ac1-139">Source</span></span>   | <span data-ttu-id="84ac1-140">目標</span><span class="sxs-lookup"><span data-stu-id="84ac1-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="84ac1-141">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="84ac1-141">MyCustomAction</span></span> | <span data-ttu-id="84ac1-142">6</span><span class="sxs-lookup"><span data-stu-id="84ac1-142">6</span></span>    | <span data-ttu-id="84ac1-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="84ac1-143">MyCA.vbs</span></span> | <span data-ttu-id="84ac1-144">MyVBScriptCA</span><span class="sxs-lookup"><span data-stu-id="84ac1-144">MyVBScriptCA</span></span> |



 

 

 



