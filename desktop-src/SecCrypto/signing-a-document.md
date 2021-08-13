---
description: 簽章的標準用途是簽署文字，並將該帶正負號的文字儲存至檔案。 簽署的文字也可透過網際網路傳送。 簽署的訊息是 PKCS \# 7 格式。
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: 簽署檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526bc4cd98d6cab40efc884a2377f3720c9849dbb7f6c1d4e8da5d49898bfa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898162"
---
# <a name="signing-a-document"></a>簽署檔

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

簽章的標準用途是簽署文字，並將該帶正負號的文字儲存至檔案。 簽署的文字也可透過網際網路傳送。 簽署的訊息是 PKCS \# 7 格式。

在此範例中，會針對卸離的內容建立簽章， (當內容未隨附于簽章) 時。 如果簽章的收件者有一份完整的帶正負號文字，最常使用卸離的簽章。 在下列範例中，會將原始訊息和卸離的簽章寫入個別的檔案。

在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。 如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。 如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。

建立簽章會使用簽署人的 [*私密金鑰*](../secgloss/p-gly.md)。 只有當簽署者的憑證有相關聯的私密金鑰可供使用時，才能建立簽章。 這個 **Sign** 方法的範例不會指定簽署人。 如果未指定簽署者，且在 **CAPICOM 我的 \_ \_ 存放區** 中沒有任何憑證有相關聯的私密金鑰，則 **Sign** 方法會失敗。 如果 **CAPICOM \_ MY \_ STORE** 中只有一個憑證有相關聯的私密金鑰，則會使用該憑證與其私密金鑰來建立簽章。 如果 [ **CAPICOM \_ MY \_ STORE** ] 存放區中有一個以上的憑證有相關聯的私密金鑰，就會出現一個對話方塊，使用者可以選擇要用來建立簽章的憑證。

當 web 應用程式使用 **Sign** 方法時，一律會顯示提示，並且需要使用者的許可權，才能建立使用該簽署者之私密金鑰的簽章。


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> <dt>

[**簽署者憑證**](signer-certificate.md)
</dt> <dt>

[**屬性**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
