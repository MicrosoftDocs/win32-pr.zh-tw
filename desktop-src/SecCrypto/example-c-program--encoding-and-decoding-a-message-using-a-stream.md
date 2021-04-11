---
description: 示範如何搭配使用 CryptMsgOpenToEncode、CryptMsgOpenToDecode 和 CryptMsgUpdate 函式和 CMSG \_ 串流 \_ 資訊結構，使用這些函式的資料流程功能來編碼和解碼訊息。
ms.assetid: 6c9c0509-1ad9-42cd-9589-e77752df6739
title: 範例 C 程式：使用資料流程編碼和解碼訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962420bfba05caabb272419e305ee01f76d39c63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691767"
---
# <a name="example-c-program-encoding-and-decoding-a-message-using-a-stream"></a><span data-ttu-id="117d8-103">範例 C 程式：使用資料流程編碼和解碼訊息</span><span class="sxs-lookup"><span data-stu-id="117d8-103">Example C Program: Encoding and Decoding a Message Using a Stream</span></span>

<span data-ttu-id="117d8-104">下列範例示範如何搭配使用 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)、 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)和 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 函式和 [**CMSG \_ 串流 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) 結構，使用這些函式的資料流程功能來編碼和解碼訊息。</span><span class="sxs-lookup"><span data-stu-id="117d8-104">The following example demonstrates how to use the [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), and [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) functions with the [**CMSG\_STREAM\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) structure to encode and decode a message using the streaming features of these functions.</span></span>

<span data-ttu-id="117d8-105">簽署及編碼訊息並不會確保該訊息的隱私權。</span><span class="sxs-lookup"><span data-stu-id="117d8-105">Signing and encoding a message does not ensure privacy for that message.</span></span> <span data-ttu-id="117d8-106">相反地，它可確保訊息的真實性。</span><span class="sxs-lookup"><span data-stu-id="117d8-106">Rather it ensures the authenticity of the message.</span></span> <span data-ttu-id="117d8-107">由於訊息是以寄件者的私密金鑰簽署，因此當訊息的接收者使用傳送者的 [*公開金鑰*](../secgloss/p-gly.md) 解密簽章時 (可從隨訊息) 傳送的憑證中取得，因此接收者可以確定訊息是由與憑證相關聯的人員或實體所傳送，而且訊息在簽署後並未變更。</span><span class="sxs-lookup"><span data-stu-id="117d8-107">Because the message is signed with the sender's private key, when the receiver of the message decrypts the signature with the sender's [*public key*](../secgloss/p-gly.md) (available from the certificate that is sent along with the message), the receiver can be sure that the message was sent by the person or entity associated with the certificate and that the message was not changed after it was signed.</span></span>

<span data-ttu-id="117d8-108">此範例的這份編碼簽署部分說明下列工作和 CryptoAPI 函數：</span><span class="sxs-lookup"><span data-stu-id="117d8-108">This encoding signing portion of this example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="117d8-109">使用 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="117d8-109">Opening a certificate store by using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="117d8-110">使用 [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)來抓取具有特定主體名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="117d8-110">Retrieving a certificate with a specific subject name by using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="117d8-111">使用 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)取得和列印憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="117d8-111">Getting and printing a certificate's subject name by using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="117d8-112">取得密碼編譯提供者的控制碼，該提供者可以使用 [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey) 函式提供私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="117d8-112">Getting the handle to a cryptographic provider that can provide a private key with the [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey) function.</span></span>
-   <span data-ttu-id="117d8-113">將 [**CMSG \_ 簽署的 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) 和 [**CMSG \_ 資料流程 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) 結構初始化，以用於 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="117d8-113">Initializing the [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) and [**CMSG\_STREAM\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) structures to be used in a call to [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span></span>
-   <span data-ttu-id="117d8-114">使用 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode) 和 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)簽署和編碼訊息。</span><span class="sxs-lookup"><span data-stu-id="117d8-114">Signing and encoding a message by using [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode) and [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="117d8-115">執行資料流程回呼函式，此函式可以使用任何持續格式來儲存編碼和簽署的訊息，例如將它寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="117d8-115">Implementing a stream callback function that can save an encoded and signed message in any persistent format, such as writing it to a file.</span></span>

<span data-ttu-id="117d8-116">此範例的解碼部分說明下列工作和 CryptoAPI 函數：</span><span class="sxs-lookup"><span data-stu-id="117d8-116">The decoding portion of this example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="117d8-117">初始化要用於呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)的 [**CMSG \_ 資料流程 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info)結構。</span><span class="sxs-lookup"><span data-stu-id="117d8-117">Initializing a [**CMSG\_STREAM\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) structure to be used in a call to [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span></span>
-   <span data-ttu-id="117d8-118">執行資料流程回呼函式，此函式可將已解碼的訊息儲存為任何持續格式，例如將它列印到螢幕。</span><span class="sxs-lookup"><span data-stu-id="117d8-118">Implementing a stream callback function that can save a decoded message in any persistent format, such as printing it to the screen.</span></span>
-   <span data-ttu-id="117d8-119">從檔案讀取編碼的訊息，並使用 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)解碼訊息。</span><span class="sxs-lookup"><span data-stu-id="117d8-119">Reading an encoded message from a file and decoding the message by using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>

<span data-ttu-id="117d8-120">如需如何在不使用資料流程回呼的情況下執行這些相同作業的範例，請參閱 [範例 C 程式：簽署、編碼、解碼和驗證訊息](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)。</span><span class="sxs-lookup"><span data-stu-id="117d8-120">For an example of how to perform these same operations without using a stream callback, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

<span data-ttu-id="117d8-121">這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。</span><span class="sxs-lookup"><span data-stu-id="117d8-121">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="117d8-122">此範例包含此函式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="117d8-122">Code for this function is included with the sample.</span></span> <span data-ttu-id="117d8-123">這項功能和其他輔助函式的程式碼也會列在 [一般 \_ 用途 \_ ](general-purpose-functions.md)的函式底下。</span><span class="sxs-lookup"><span data-stu-id="117d8-123">Code for this and other auxiliary functions is also listed under [General\_Purpose\_Functions](general-purpose-functions.md).</span></span>


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

#define MAX_NAME 256

#define ENCODED_FILE_NAME L"testStream.p7s"

//-------------------------------------------------------------------
//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

//+----------------------------------------------
// Callback function used for streamed Signing. 
//-----------------------------------------------
BOOL 
WINAPI
EncodeCallback(
    const void *pvArg,
    BYTE *pbData,
    DWORD cbData,
    BOOL fFinal)
{
    DWORD dwWrittenBytes = 0;
    HANDLE hFileToWrite = INVALID_HANDLE_VALUE;
        
    hFileToWrite = *((HANDLE *)pvArg);
    if ( !WriteFile(
            hFileToWrite,
            pbData,
            cbData,
            &dwWrittenBytes,
            NULL) ||
        (dwWrittenBytes != cbData))
    {
        return FALSE;
    }

    return TRUE;
}

//+----------------------------------------------
// Callback function used for decoding streamed Signing.
//-----------------------------------------------
BOOL 
WINAPI
DecodeCallback(
    const void *pvArg,
    BYTE *pbData,
    DWORD cbData,
    BOOL fFinal)
{
    if (pbData != NULL && cbData > 0)
    {
        *(pbData+cbData) = 0;
        printf("%s", (char*)pbData);
    }

    return TRUE;
}

void EncodeMessageWithStream(LPWSTR pwszSignerName)
{
    //---------------------------------------------------------------
    // Declare and initialize variables. This includes declaring and 
    // initializing a pointer to message content to be countersigned 
    // and encoded. Usually, the message content will exist somewhere
    // and a pointer to it is passed to the application. 

    BYTE* pbContent1 = (BYTE*)"First sentence. ";
    DWORD cbContent1 = lstrlenA((char *)pbContent1);
    BYTE* pbContent2 = (BYTE*)"Second sentence. ";
    DWORD cbContent2 = lstrlenA((char *)pbContent2);

    HCRYPTPROV hCryptProv;         // CSP handle
    HCERTSTORE hStoreHandle;       // store handle
    PCCERT_CONTEXT pSignerCert;    // signer certificate
    CMSG_SIGNER_ENCODE_INFO SignerEncodeInfo;
    CMSG_SIGNER_ENCODE_INFO SignerEncodeInfoArray[1];
    CERT_BLOB SignerCertBlob;
    CERT_BLOB SignerCertBlobArray[1];
    CMSG_SIGNED_ENCODE_INFO SignedMsgEncodeInfo;
    HCRYPTMSG hMsg;
    LPWSTR pszNameString;
    DWORD dwKeySpec;

    //---------------------------------------------------------------
    // Open the My system certificate store.

    if(!(hStoreHandle = CertOpenStore(
        // The system store will be a virtual store.
        CERT_STORE_PROV_SYSTEM,
        // Encoding type not needed with this PROV.
        0,
        // Accept the default HCRYPTPROV. 
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        // Set the system store location in the registry. Other 
        // predefined system stores could have been used, including 
        // trust, Ca, or root.
        L"MY")))                
    {
        MyHandleError(L"Could not open the MY system store.");
    }

    //---------------------------------------------------------------
    // Get a pointer to a signer's signature certificate.

    if(pSignerCert = CertFindCertificateInStore(
        hStoreHandle,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        pwszSignerName,
        NULL))
    {
        //-----------------------------------------------------------
        //   A certificate was found. Get and print the name of the 
        //   subject of the certificate.

        if(CertGetNameString(
            pSignerCert,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszNameString,
            MAX_NAME) > 1)
        {
            printf("The message signer is  %s \n",pszNameString);
        }
        else
        {
            MyHandleError(L"CertGetNameString failed.\n");
        }
    }
    else
    {
        MyHandleError(L"Cert not found.\n");
    }

    //---------------------------------------------------------------
    // Initialize the CMSG_SIGNER_ENCODE_INFO structure.

    //---------------------------------------------------------------
    // Get a handle to a cryptographic provider. 
    if(!(CryptAcquireCertificatePrivateKey(
        pSignerCert,
        0,
        NULL,
        &hCryptProv,
        &dwKeySpec,
        NULL)))
    {
        DWORD dwError = GetLastError();
        if(NTE_BAD_PUBLIC_KEY == dwError)
        {
            printf("NTE_BAD_PUBLIC_KEY\n");
        }

        MyHandleError(L"CryptAcquireContext failed");
    }
     
    memset(&SignerEncodeInfo, 0, sizeof(CMSG_SIGNER_ENCODE_INFO));
    SignerEncodeInfo.cbSize = sizeof(CMSG_SIGNER_ENCODE_INFO);
    SignerEncodeInfo.pCertInfo = pSignerCert->pCertInfo;
    SignerEncodeInfo.hCryptProv = hCryptProv;
    SignerEncodeInfo.dwKeySpec = dwKeySpec;
    SignerEncodeInfo.HashAlgorithm.pszObjId = szOID_RSA_MD5;
    SignerEncodeInfo.pvHashAuxInfo = NULL;

    //---------------------------------------------------------------
    // Initialize the first element of an array of signers. 
    // Note: Currently, there is only one signer.

    SignerEncodeInfoArray[0] = SignerEncodeInfo;

    //---------------------------------------------------------------
    // Initialize the CMSG_SIGNED_ENCODE_INFO structure.

    SignerCertBlob.cbData = pSignerCert->cbCertEncoded;
    SignerCertBlob.pbData = pSignerCert->pbCertEncoded;

    //---------------------------------------------------------------
    //  Initialize the first element of an array of signer BLOBs.
    //  Note: In this program, there is only one signer BLOB used.

    SignerCertBlobArray[0] = SignerCertBlob;
    memset(&SignedMsgEncodeInfo, 0, sizeof(CMSG_SIGNED_ENCODE_INFO));
    SignedMsgEncodeInfo.cbSize = sizeof(CMSG_SIGNED_ENCODE_INFO);
    SignedMsgEncodeInfo.cSigners = 1;
    SignedMsgEncodeInfo.rgSigners = SignerEncodeInfoArray;
    SignedMsgEncodeInfo.cCertEncoded = 1;
    SignedMsgEncodeInfo.rgCertEncoded = SignerCertBlobArray;

    // Fill the CMSG_STREAM_INFO structure.
    CMSG_STREAM_INFO stStreamInfo;

    // BER_ENCODING
    stStreamInfo.cbContent = 0xffffffff;
    // DER_ENCODING 
    // stStreamInfo.cbContent = cbContent;

    stStreamInfo.pfnStreamOutput = EncodeCallback;
    HANDLE hOutMsgFile = INVALID_HANDLE_VALUE;
    hOutMsgFile = CreateFile(
            ENCODED_FILE_NAME,
            GENERIC_WRITE,
            FILE_SHARE_WRITE,
            NULL,
            CREATE_ALWAYS,
            FILE_ATTRIBUTE_NORMAL,
            NULL);
    if (INVALID_HANDLE_VALUE == hOutMsgFile)
    {
        MyHandleError(L"CreateFile (OUT MSG)");
    }

    stStreamInfo.pvArg = &hOutMsgFile; 

    //---------------------------------------------------------------
    // Open a message to encode.

    if(!(hMsg = CryptMsgOpenToEncode(
        MY_ENCODING_TYPE,      // encoding type
        0,                     // flags
        CMSG_SIGNED,           // message type
        &SignedMsgEncodeInfo,  // pointer to structure
        NULL,                  // inner content OID
        &stStreamInfo)))       // stream information
    {
        MyHandleError(L"OpenToEncode failed");
    }

    //---------------------------------------------------------------
    // Update the message with the data.

    if(!(CryptMsgUpdate(
        hMsg,        // handle to the message
        pbContent1,  // pointer to the content
        cbContent1,  // size of the content
        FALSE)))     // first call
    {
        MyHandleError(L"MsgUpdate failed");
    }

    if(!(CryptMsgUpdate(
        hMsg,        // handle to the message
        pbContent2,  // pointer to the content
        cbContent2,  // size of the content
        TRUE)))      // last call
    {
        MyHandleError(L"MsgUpdate failed");
    }

    //---------------------------------------------------------------
    // The message is signed and encoded.
    // Close the message handle and the certificate store.

    CryptMsgClose(hMsg);
    CertCloseStore(hStoreHandle, CERT_CLOSE_STORE_FORCE_FLAG);
    CryptReleaseContext(hCryptProv,0);
    CloseHandle(hOutMsgFile);
}

void DecodeMessageWithStream()
{
    //---------------------------------------------------------------
    // Open the message for decoding.

    HCRYPTMSG hMsg;

    // Fill the CMSG_STREAM_INFO structure.
    CMSG_STREAM_INFO stStreamInfo2;

    // BER_ENCODING
    stStreamInfo2.cbContent = 0xffffffff;
    stStreamInfo2.pfnStreamOutput = DecodeCallback;

    if(!(hMsg = CryptMsgOpenToDecode(
        MY_ENCODING_TYPE,   // encoding type
        0,                  // flags
        0,                  // message type (get from message)
        NULL,               // cryptographic provider
                            // use NULL for the default provider
        NULL,               // recipient information
        &stStreamInfo2)))   // stream information
    {
        MyHandleError(L"OpenToDecode failed.");
    }

    HANDLE hInMsgFile = INVALID_HANDLE_VALUE;
    hInMsgFile = CreateFile(
            ENCODED_FILE_NAME,
            GENERIC_READ,
            FILE_SHARE_READ,
            NULL,
            OPEN_EXISTING,
            FILE_ATTRIBUTE_NORMAL,
            NULL);
    if (INVALID_HANDLE_VALUE == hInMsgFile)
    {
        MyHandleError(L"CreateFile (IN MSG)");
    }

    const DWORD cbBytesToRead = 256;
    byte pbEncodedBlob[cbBytesToRead];
    DWORD cbBytesRead;
    BOOL lastCall = FALSE;

    while (ReadFile(
        hInMsgFile,
        pbEncodedBlob,
        cbBytesToRead,
        &cbBytesRead,
        NULL))
    {
        if (cbBytesRead < cbBytesToRead)
        {
            lastCall = TRUE;
        }

        if(!(CryptMsgUpdate(
            hMsg,            // handle to the message
            pbEncodedBlob,   // pointer to the encoded BLOB
            cbBytesRead,     // size of the encoded BLOB
            lastCall)))      // last call
        {
            MyHandleError(L"Decode MsgUpdate failed.");
        }

        if (lastCall)
        {
            break;
        }
    }

    CryptMsgClose(hMsg);
    CloseHandle(hInMsgFile);
}
```



 

 
