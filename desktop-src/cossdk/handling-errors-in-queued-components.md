---
description: 有時候，發生訊息無法成功傳遞至其預定目的地的情況，通常是因為系統或設定發生問題。
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: 處理已排入佇列之元件中的錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510629"
---
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="b3d13-103">處理已排入佇列之元件中的錯誤</span><span class="sxs-lookup"><span data-stu-id="b3d13-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="b3d13-104">有時候，發生訊息無法成功傳遞至其預定目的地的情況，通常是因為系統或設定發生問題。</span><span class="sxs-lookup"><span data-stu-id="b3d13-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="b3d13-105">例如，訊息可能會被導向至不存在的佇列，或目的地佇列可能不是要接收的狀態。</span><span class="sxs-lookup"><span data-stu-id="b3d13-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="b3d13-106">訊息移動器是一種工具，可將所有失敗的 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 訊息從一個佇列移至另一個佇列，以便重試。</span><span class="sxs-lookup"><span data-stu-id="b3d13-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="b3d13-107">訊息移動器公用程式是可利用 VBScript 叫用的自動化物件。</span><span class="sxs-lookup"><span data-stu-id="b3d13-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="b3d13-108">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="b3d13-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="b3d13-109">不適用。</span><span class="sxs-lookup"><span data-stu-id="b3d13-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="b3d13-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b3d13-110">Visual Basic</span></span>

<span data-ttu-id="b3d13-111">下列範例程式碼示範如何建立 MessageMover 物件、設定所需的屬性，以及起始傳送。</span><span class="sxs-lookup"><span data-stu-id="b3d13-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="b3d13-112">若要從 Visual Basic 使用它，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="b3d13-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="b3d13-113">若要使用 MessageMover 物件，您必須在電腦上安裝訊息佇列，而且 AppName 指定的應用程式必須啟用佇列。</span><span class="sxs-lookup"><span data-stu-id="b3d13-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="b3d13-114">如需安裝訊息佇列的相關資訊，請參閱 [ **開始** ] 功能表上的 [說明及支援]。</span><span class="sxs-lookup"><span data-stu-id="b3d13-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



<span data-ttu-id="b3d13-115">下列 Visual Basic 程式碼會示範如何呼叫 MyMessageMover 函數。</span><span class="sxs-lookup"><span data-stu-id="b3d13-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="b3d13-116">訊息的來源路徑是最後的靜止佇列。</span><span class="sxs-lookup"><span data-stu-id="b3d13-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="b3d13-117">它是不正確佇列，也就是私用訊息佇列的佇列，而且稱為 AppName \_ deadqueue。</span><span class="sxs-lookup"><span data-stu-id="b3d13-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="b3d13-118">如果交易在第五次重試佇列上嘗試時重複中止，則會在這裡移動訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d13-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="b3d13-119">使用訊息移動器工具，您可以將訊息移回第一個佇列，稱為 AppName。</span><span class="sxs-lookup"><span data-stu-id="b3d13-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="b3d13-120">如需重試佇列的詳細資訊，請參閱 [伺服器端錯誤](server-side-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="b3d13-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="b3d13-121">如果佇列屬性允許，訊息移動器會將訊息 transitionally，以便在移動期間發生失敗時，不會遺失或重複訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d13-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="b3d13-122">此工具會保留將訊息從一個佇列移至另一個佇列時可保留的所有訊息屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d13-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="b3d13-123">如果訊息是由 COM + 佇列元件呼叫所產生，訊息移動器公用程式會在佇列之間移動訊息時，保留原始呼叫端的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3d13-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="b3d13-124">如果目的地和來源佇列都是交易式，則整個作業都會 transitionally 完成。</span><span class="sxs-lookup"><span data-stu-id="b3d13-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="b3d13-125">如果來源或目的地佇列不是交易式，則作業不會在交易下執行。</span><span class="sxs-lookup"><span data-stu-id="b3d13-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="b3d13-126">非預期的失敗 (例如損毀) 和重新開機非交易式移動，可能會在失敗時複製正在移動的訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d13-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="b3d13-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="b3d13-127">C/C++</span></span>

<span data-ttu-id="b3d13-128">下列範例程式碼示範如何建立 MessageMover 物件、設定所需的屬性，以及起始傳送。</span><span class="sxs-lookup"><span data-stu-id="b3d13-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="b3d13-129">ErrorDescription 方法說明于 [解釋錯誤碼](interpreting-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="b3d13-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="b3d13-130">若要使用 MessageMover 物件，您必須在電腦上安裝訊息佇列，而且 AppName 指定的應用程式必須啟用佇列。</span><span class="sxs-lookup"><span data-stu-id="b3d13-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="b3d13-131">如需安裝訊息佇列的相關資訊，請參閱 [ **開始** ] 功能表上的 [說明及支援]。</span><span class="sxs-lookup"><span data-stu-id="b3d13-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



<span data-ttu-id="b3d13-132">下列 c + + 程式碼示範如何呼叫 MyMessageMover 函數。</span><span class="sxs-lookup"><span data-stu-id="b3d13-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



<span data-ttu-id="b3d13-133">訊息的來源路徑是最後的靜止佇列。</span><span class="sxs-lookup"><span data-stu-id="b3d13-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="b3d13-134">它是不正確佇列，也就是私用訊息佇列的佇列，而且稱為 AppName \_ deadqueue。</span><span class="sxs-lookup"><span data-stu-id="b3d13-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="b3d13-135">如果交易在第五次重試佇列上嘗試時重複中止，則會在這裡移動訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d13-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="b3d13-136">使用訊息移動器工具，您可以將訊息移回第一個佇列，稱為 AppName。</span><span class="sxs-lookup"><span data-stu-id="b3d13-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="b3d13-137">如需重試佇列的詳細資訊，請參閱 [伺服器端錯誤](server-side-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="b3d13-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="b3d13-138">如果佇列屬性允許，訊息移動器會將訊息 transitionally，以便在移動期間發生失敗時，不會遺失或重複訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d13-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="b3d13-139">此工具會保留將訊息從一個佇列移至另一個佇列時可保留的所有訊息屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d13-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="b3d13-140">如果訊息是由 COM + 佇列元件呼叫所產生，訊息移動器公用程式會在佇列之間移動訊息時，保留原始呼叫端的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3d13-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="b3d13-141">如果目的地和來源佇列都是交易式，則整個作業都會 transitionally 完成。</span><span class="sxs-lookup"><span data-stu-id="b3d13-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="b3d13-142">如果來源或目的地佇列不是交易式，則作業不會在交易下執行。</span><span class="sxs-lookup"><span data-stu-id="b3d13-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="b3d13-143">非預期的失敗 (例如損毀) 和重新開機非交易式移動，可能會在失敗時複製正在移動的訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d13-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d13-144">備註</span><span class="sxs-lookup"><span data-stu-id="b3d13-144">Remarks</span></span>

<span data-ttu-id="b3d13-145">COM + 會藉由將失敗的訊息移至不同的「最後離開」佇列來處理伺服器端 (播放機) 中止，以使其無法運作。</span><span class="sxs-lookup"><span data-stu-id="b3d13-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="b3d13-146">接聽程式和播放程式無法持續在中止的訊息上迴圈。</span><span class="sxs-lookup"><span data-stu-id="b3d13-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="b3d13-147">在許多情況下，您可以在伺服器上採取動作來修正中止的交易。</span><span class="sxs-lookup"><span data-stu-id="b3d13-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3d13-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3d13-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3d13-149">佇列元件錯誤</span><span class="sxs-lookup"><span data-stu-id="b3d13-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 



