---
description: 當收到簽署的檔時，可以檢查簽章或簽章的有效性。
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: 驗證檔上的簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb1e6bbec678f74c9761c7f4c0712249c8b557a68b5e9f80aeeb3306faede36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970932"
---
# <a name="verifying-the-signature-on-a-document"></a>驗證檔上的簽章

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

當收到簽署的檔時，可以檢查簽章或簽章的有效性。 簽章可以檢查：

-   簽章雜湊的有效性
-   簽署者憑證的有效性

簽章 [*雜湊*](../secgloss/h-gly.md)會使用簽署者 [*憑證*](../secgloss/c-gly.md)上找到之簽署者的 [*公開金鑰*](../secgloss/p-gly.md)進行解密，並納入為簽章的一部分。 如果解密簽章符合原始檔案的新雜湊，則簽章是由與用來解密雜湊的公開金鑰相關聯之私密金鑰的擁有者所建立。 此外，簽章所依據的檔，一定不會在建立簽章之後變更。

提供公開金鑰和簽署者身分識別的憑證也可以檢查是否有效，包括是否已撤銷憑證、憑證是否過期，或是憑證是否由受信任的憑證簽發者所發出。

在下列範例中，會在檔案和簽章中讀取已簽署的內容和 **SignedData** 物件，並檢查用來建立簽章之憑證的有效性。

> [!Note]  
> 如果簽章未以密碼編譯有效，或簽署者的憑證無效，則會引發例外狀況，而且驗證程式必須處理例外狀況。 在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。 如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。 如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
