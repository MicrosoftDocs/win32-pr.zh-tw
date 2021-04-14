---
description: 在下列範例中，會從檔案中讀取純文字訊息，並開啟包含預定訊息收件者憑證的憑證存放區。
ms.assetid: 7ae672d3-e11d-453c-b9c0-354d21830ae4
title: 傳送封包的資料訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c04418a2f1d0186ddc0d88c30e7cc790c715b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386211"
---
# <a name="sending-an-enveloped-data-message"></a><span data-ttu-id="74792-103">傳送封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="74792-103">Sending an Enveloped Data Message</span></span>

<span data-ttu-id="74792-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="74792-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="74792-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="74792-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="74792-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="74792-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="74792-107">在下列範例中，會從檔案中讀取純文字訊息，並開啟包含預定訊息收件者憑證的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="74792-107">In the following example, a plaintext message is read in from a file, and a certificate store that contains the certificates of the intended message recipients is opened.</span></span> <span data-ttu-id="74792-108">存放區中的所有憑證都會新增為郵件的收件者、封包訊息，然後將封包訊息寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="74792-108">All of the certificates in the store are added as recipients of the message, the message is enveloped, and the enveloped message is written to a file.</span></span>

<span data-ttu-id="74792-109">您可以新增額外的程式碼，以顯示新增為訊息收件者的憑證，以在將憑證新增為預定收件者之前先驗證這些憑證，或選擇要加入的憑證。</span><span class="sxs-lookup"><span data-stu-id="74792-109">Additional code can be added to display the certificates being added as message recipients, to verify those certificates before they are added as intended recipients, or to otherwise choose those that are to be added.</span></span>

<span data-ttu-id="74792-110">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="74792-110">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="74792-111">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="74792-111">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="74792-112">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="74792-112">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub Envelope(ByVal InFile As String, ByVal OutFile As String, _
             ByVal StoreName As String)

On Error GoTo ErrorHandler

'Open the input file and read the message to be enveloped.

Dim Text As String
Open InFile For Input As #1
Input #1, Text
Close #1
If Len(Text) < 1 Then
    MsgBox "No message to be enveloped."
    Exit Sub
End If

'Open the store containing the certificates of
'the message recipients.

Dim CertStore As New Store
CertStore.Open CAPICOM_CURRENT_USER_STORE, StoreName, _
    CAPICOM_STORE_OPEN_READ_ONLY

' Check for an empty certificate store.

If CertStore.Certificates.Count < 1 Then
    MsgBox "There are no recipient certificates available."
    Set CertStore = Nothing
    Exit Sub
End If

' Declare and initialize an EnvelopedData object

Dim EnvMessage As New EnvelopedData
EnvMessage.Content = Text
Dim I As Integer
For I = 1 To CertStore.Certificates.Count
    EnvMessage.Recipients.Add CertStore.Certificates.Item(I)
    ' The following line can be uncommented to see a prompt
    ' for each certificate in the store.
    ' CertStore.Certificates.Item(I).Display
Next I

'  Set the encryption algorithm and key length. Comment out
'  or remove the following lines to use the default algorithm
'  and key length. The triple DES algorithm and 128 bit key
'  length may not be supported.
Envmessage.Algorithm.Name = ENCRYPTION_ALGORITHM_RC4
Envmessage.Algorithm.KeyLength = KEY_LENGTH_128_BITS

'Declare the string that will hold the enveloped message.

Dim EnvelopedMessage As String

'Encrypt the message into EnvelopedMessage. The enveloped message
'string contains everything that an intended recipient will need to
'decrypt the message, including information on the 
'encryption algorithm key length.
EnvelopedMessage = EnvMessage.Encrypt

' Optionally, check the length of the encrypted string to make sure 
' that the encrypt method worked.

If Len(EnvelopedMessage) < 1 Then
    MsgBox "no message encrypted. "
Else
    MsgBox " Message is " & Len(EnvelopedMessage) & " characters"

    ' Open an output file and write the encrypted message to the 
    ' file. The file is not opened if there is no message to write.
    Open OutFile For Output As #2
    Write #2, EnvelopedMessage
    Close #2
    MsgBox "The message written to file "
End If

' Release the EncryptedData object and the Store object.
Set Envmessage = Nothing
Set CertStore = Nothing

Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found : " & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 



