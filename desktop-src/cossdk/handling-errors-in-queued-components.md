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
# <a name="handling-errors-in-queued-components"></a>處理已排入佇列之元件中的錯誤

有時候，發生訊息無法成功傳遞至其預定目的地的情況，通常是因為系統或設定發生問題。 例如，訊息可能會被導向至不存在的佇列，或目的地佇列可能不是要接收的狀態。 訊息移動器是一種工具，可將所有失敗的 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 訊息從一個佇列移至另一個佇列，以便重試。 訊息移動器公用程式是可利用 VBScript 叫用的自動化物件。

## <a name="components-services-administrative-tool"></a>元件服務系統管理工具

不適用。

## <a name="visual-basic"></a>Visual Basic

下列範例程式碼示範如何建立 MessageMover 物件、設定所需的屬性，以及起始傳送。 若要從 Visual Basic 使用它，請新增 COM + 服務類型程式庫的參考。

> [!Note]  
> 若要使用 MessageMover 物件，您必須在電腦上安裝訊息佇列，而且 AppName 指定的應用程式必須啟用佇列。 如需安裝訊息佇列的相關資訊，請參閱 [ **開始** ] 功能表上的 [說明及支援]。

 


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



下列 Visual Basic 程式碼會示範如何呼叫 MyMessageMover 函數。


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



訊息的來源路徑是最後的靜止佇列。 它是不正確佇列，也就是私用訊息佇列的佇列，而且稱為 AppName \_ deadqueue。 如果交易在第五次重試佇列上嘗試時重複中止，則會在這裡移動訊息。 使用訊息移動器工具，您可以將訊息移回第一個佇列，稱為 AppName。 如需重試佇列的詳細資訊，請參閱 [伺服器端錯誤](server-side-errors.md)。

如果佇列屬性允許，訊息移動器會將訊息 transitionally，以便在移動期間發生失敗時，不會遺失或重複訊息。 此工具會保留將訊息從一個佇列移至另一個佇列時可保留的所有訊息屬性。

如果訊息是由 COM + 佇列元件呼叫所產生，訊息移動器公用程式會在佇列之間移動訊息時，保留原始呼叫端的安全識別碼。 如果目的地和來源佇列都是交易式，則整個作業都會 transitionally 完成。 如果來源或目的地佇列不是交易式，則作業不會在交易下執行。 非預期的失敗 (例如損毀) 和重新開機非交易式移動，可能會在失敗時複製正在移動的訊息。

## <a name="cc"></a>C/C++

下列範例程式碼示範如何建立 MessageMover 物件、設定所需的屬性，以及起始傳送。 ErrorDescription 方法說明于 [解釋錯誤碼](interpreting-error-codes.md)。

> [!Note]  
> 若要使用 MessageMover 物件，您必須在電腦上安裝訊息佇列，而且 AppName 指定的應用程式必須啟用佇列。 如需安裝訊息佇列的相關資訊，請參閱 [ **開始** ] 功能表上的 [說明及支援]。

 


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



下列 c + + 程式碼示範如何呼叫 MyMessageMover 函數。


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



訊息的來源路徑是最後的靜止佇列。 它是不正確佇列，也就是私用訊息佇列的佇列，而且稱為 AppName \_ deadqueue。 如果交易在第五次重試佇列上嘗試時重複中止，則會在這裡移動訊息。 使用訊息移動器工具，您可以將訊息移回第一個佇列，稱為 AppName。 如需重試佇列的詳細資訊，請參閱 [伺服器端錯誤](server-side-errors.md)。

如果佇列屬性允許，訊息移動器會將訊息 transitionally，以便在移動期間發生失敗時，不會遺失或重複訊息。 此工具會保留將訊息從一個佇列移至另一個佇列時可保留的所有訊息屬性。

如果訊息是由 COM + 佇列元件呼叫所產生，訊息移動器公用程式會在佇列之間移動訊息時，保留原始呼叫端的安全識別碼。 如果目的地和來源佇列都是交易式，則整個作業都會 transitionally 完成。 如果來源或目的地佇列不是交易式，則作業不會在交易下執行。 非預期的失敗 (例如損毀) 和重新開機非交易式移動，可能會在失敗時複製正在移動的訊息。

## <a name="remarks"></a>備註

COM + 會藉由將失敗的訊息移至不同的「最後離開」佇列來處理伺服器端 (播放機) 中止，以使其無法運作。 接聽程式和播放程式無法持續在中止的訊息上迴圈。 在許多情況下，您可以在伺服器上採取動作來修正中止的交易。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[佇列元件錯誤](queued-components-errors.md)
</dt> </dl>

 

 



