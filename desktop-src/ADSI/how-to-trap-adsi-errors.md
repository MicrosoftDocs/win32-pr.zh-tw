---
title: 如何陷阱 ADSI 錯誤
description: VBScript 只提供一種方式來捕捉錯誤內嵌錯誤處理。
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967802"
---
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="3b323-103">如何陷阱 ADSI 錯誤</span><span class="sxs-lookup"><span data-stu-id="3b323-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="3b323-104">VBScript 只提供一種方式來捕捉錯誤：內嵌錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="3b323-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="3b323-105">內嵌錯誤處理常式的開頭為 **On Error Resume Next** 語句。</span><span class="sxs-lookup"><span data-stu-id="3b323-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="3b323-106">由於 **在錯誤** 繼續之後，接下來將會防止任何錯誤停止執行腳本，直到 **下次發生錯誤繼續** 的範圍結束為止。您 **必須在發生** 錯誤時 **繼續下** 一個語句的每個點，檢查錯誤的值。</span><span class="sxs-lookup"><span data-stu-id="3b323-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="3b323-107">下列範例示範 ADSI 腳本中的內嵌錯誤處理：</span><span class="sxs-lookup"><span data-stu-id="3b323-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



<span data-ttu-id="3b323-108">在腳本可能遇到錯誤的每個位置之後，就會有 **If Err** 語句。</span><span class="sxs-lookup"><span data-stu-id="3b323-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="3b323-109">**Err** 物件包含執行腳本期間發生之最後一個錯誤的錯誤碼;如果未發生錯誤，則 **Err** 一律為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="3b323-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="3b323-110">在上述範例中，錯誤會導致執行跳至 **AdsiErr** 副程式，以檢查錯誤的值 **是否為預期的錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="3b323-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="3b323-111">除了定生死的錯誤訊息之外，腳本還會對它停止執行的原因提供更好的說明。</span><span class="sxs-lookup"><span data-stu-id="3b323-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="3b323-112">請記住，在 [發生 **錯誤時繼續] 下** 的範圍中，會呼叫 [發生錯誤時 **繼續] 下一個呼叫之後** 發生的任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b323-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="3b323-113">如果您忘記在適當的位置檢查 **錯誤** 的值，這實際上會讓腳本更難進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="3b323-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="3b323-114">無論您預期發生錯誤的位置，請務必檢查 **錯誤的值。**</span><span class="sxs-lookup"><span data-stu-id="3b323-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="3b323-115"> (當您一開始對腳本進行偵錯工具時，您可能會想要讓腳本停止執行，並顯示錯誤的問題行號，然後在基本程式流程正確之後加入錯誤處理常式。 ) </span><span class="sxs-lookup"><span data-stu-id="3b323-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 




