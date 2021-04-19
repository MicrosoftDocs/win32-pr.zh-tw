---
description: 檔可由一個以上的簽署者簽署。
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosigning 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974781"
---
# <a name="cosigning-a-document"></a>Cosigning 檔

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

檔可由一個以上的簽署者簽署。 例如，當兩個或更多方簽署合約或支出報表時，就會發生這種情況。 在下列範例中，已簽署的檔是由第二位簽署者所接收。 這個簽署者會使用 [**CoSign**](signeddata-cosign.md) 方法，將其他簽章附加至檔。

如果發生任何 CAPICOM 錯誤，則會在 **Err** 屬性中傳回負數值。 如需有關 CAPICOM 錯誤碼的詳細資訊，請參閱 [**capicom \_ 錯誤碼 \_**](capicom-error-code.md)。 如果 **Err** 屬性中的錯誤碼是正值，則錯誤是 Windows 錯誤。 如需 Windows 錯誤碼的詳細資訊，請參閱 Winerror.h。

> [!Note]
> Cosigning 檔時，也需要 cosigner 擁有具有 [*私密金鑰*](../secgloss/p-gly.md)的可用 [*憑證*](../secgloss/c-gly.md)，才能建立簽章。 如果未在 [**Sign**](signeddata-sign.md) 方法的呼叫中指定簽署者，且在 \_ 具有相關私密金鑰的 CAPICOM MY 存放區中沒有憑證 \_ ，則方法會失敗。 如果在具有相關私密金鑰的 CAPICOM MY STORE 中只有一個憑證 \_ \_ ，則會使用該金鑰和憑證。 如果有一個以上的可用憑證，則會顯示提示，讓使用者選擇所需的憑證。
> 
> 如果在 web 應用程式中使用 [**CoSign**](signeddata-cosign.md) 方法，則在使用該簽署者的私密金鑰建立簽章之前，一律會顯示提示以取得使用者的許可權。

 

在下列範例中，包含要簽署之檔的檔案，以及該檔的目前簽章都會被讀取、簽章為 cosigned，而新的簽章會寫入檔案。 此範例會使用已中斷連結的簽章，並將資料簽章和簽章放在不同的檔案中。


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
