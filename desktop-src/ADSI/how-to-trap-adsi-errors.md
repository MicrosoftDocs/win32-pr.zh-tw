---
title: 如何陷阱 ADSI 錯誤
description: VBScript 只提供一種方式來捕捉錯誤內嵌錯誤處理。
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082532"
---
# <a name="how-to-trap-adsi-errors"></a>如何陷阱 ADSI 錯誤

VBScript 只提供一種方式來捕捉錯誤：內嵌錯誤處理。 內嵌錯誤處理常式的開頭為 **On Error Resume Next** 語句。 由於 **在錯誤** 繼續之後，接下來將會防止任何錯誤停止執行腳本，直到 **下次發生錯誤繼續** 的範圍結束為止。您 **必須在發生** 錯誤時 **繼續下** 一個語句的每個點，檢查錯誤的值。 下列範例示範 ADSI 腳本中的內嵌錯誤處理：


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



在腳本可能遇到錯誤的每個位置之後，就會有 **If Err** 語句。 **Err** 物件包含執行腳本期間發生之最後一個錯誤的錯誤碼;如果未發生錯誤，則 **Err** 一律為零 (0) 。 在上述範例中，錯誤會導致執行跳至 **AdsiErr** 副程式，以檢查錯誤的值 **是否為預期的錯誤** 。 除了定生死的錯誤訊息之外，腳本還會對它停止執行的原因提供更好的說明。

請記住，在 [發生 **錯誤時繼續] 下** 的範圍中，會呼叫 [發生錯誤時 **繼續] 下一個呼叫之後** 發生的任何錯誤。 如果您忘記在適當的位置檢查 **錯誤** 的值，這實際上會讓腳本更難進行偵錯工具。 無論您預期發生錯誤的位置，請務必檢查 **錯誤的值。**

 (當您一開始對腳本進行偵錯工具時，您可能會想要讓腳本停止執行，並顯示錯誤的問題行號，然後在基本程式流程正確之後加入錯誤處理常式。 ) 

 

 




