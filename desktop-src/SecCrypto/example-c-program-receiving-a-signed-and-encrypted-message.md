---
description: 下列範例會與範例 C 程式：傳送和接收已簽署和已加密訊息的程式搭配使用。 它會讀取已簽署和加密的訊息，然後將訊息解密並進行驗證。
ms.assetid: 65ca30ba-a184-46ef-808c-e2fedcc86079
title: 範例 C 程式：接收已簽署和加密的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1d97b50eb401568ebf1732f347f800eed0c26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944633"
---
# <a name="example-c-program-receiving-a-signed-and-encrypted-message"></a><span data-ttu-id="42338-104">範例 C 程式：接收已簽署和加密的訊息</span><span class="sxs-lookup"><span data-stu-id="42338-104">Example C Program: Receiving a Signed and Encrypted Message</span></span>

<span data-ttu-id="42338-105">下列範例會與 [範例 C 程式：傳送和接收已簽署和已加密訊息](example-c-program-sending-and-receiving-a-signed-and-encrypted-message.md)的程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="42338-105">The following example works in conjunction with the program in [Example C Program: Sending and Receiving a Signed and Encrypted Message](example-c-program-sending-and-receiving-a-signed-and-encrypted-message.md).</span></span> <span data-ttu-id="42338-106">它會讀取已簽署和加密的訊息，然後將訊息解密並進行驗證。</span><span class="sxs-lookup"><span data-stu-id="42338-106">It reads the signed and encrypted message, then decrypts and verifies the message.</span></span>

<span data-ttu-id="42338-107">若要解密並驗證訊息，訊息的預期接收者的 [*私密金鑰*](../secgloss/p-gly.md) 必須可供使用。</span><span class="sxs-lookup"><span data-stu-id="42338-107">To decrypt and verify the message, the [*private key*](../secgloss/p-gly.md) of the message's intended receiver must be available.</span></span> <span data-ttu-id="42338-108">簽署者的憑證包含在從檔案讀取的訊息 [*BLOB*](../secgloss/b-gly.md) 中。</span><span class="sxs-lookup"><span data-stu-id="42338-108">The certificate of the signer is included in the message [*BLOB*](../secgloss/b-gly.md) read in from the file.</span></span>

<span data-ttu-id="42338-109">此範例說明下列工作：</span><span class="sxs-lookup"><span data-stu-id="42338-109">This example illustrates the following tasks:</span></span>

-   <span data-ttu-id="42338-110">開啟和關閉系統憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="42338-110">Opening and closing system certificate stores.</span></span>
-   <span data-ttu-id="42338-111">從檔案讀取 [**CERT \_ 名稱 \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="42338-111">Reading a [**CERT\_NAME\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) from a file.</span></span>
-   <span data-ttu-id="42338-112">初始化解密和驗證訊息所需的資料結構。</span><span class="sxs-lookup"><span data-stu-id="42338-112">Initializing data structures needed to decrypt and verify a message.</span></span>
-   <span data-ttu-id="42338-113">呼叫 CryptoAPI 函式以找出所需的緩衝區大小，配置所需大小的緩衝區，然後再次呼叫 CryptoAPI 函式來填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="42338-113">Calling a CryptoAPI function to find the required size of a buffer, allocating the buffer of the required size, and calling the CryptoAPI function again to fill the buffer.</span></span> <span data-ttu-id="42338-114">如需詳細資訊，請參閱 [取出未知長度的資料](retrieving-data-of-unknown-length.md)。</span><span class="sxs-lookup"><span data-stu-id="42338-114">For more information, see [Retrieving Data of Unknown Length](retrieving-data-of-unknown-length.md).</span></span>

<span data-ttu-id="42338-115">此範例使用下列 CryptoAPI 函數：</span><span class="sxs-lookup"><span data-stu-id="42338-115">This example uses the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="42338-116">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="42338-116">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [<span data-ttu-id="42338-117">**CryptDecryptAndVerifyMessageSignature**</span><span class="sxs-lookup"><span data-stu-id="42338-117">**CryptDecryptAndVerifyMessageSignature**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature)
-   [<span data-ttu-id="42338-118">**CertCloseStore**</span><span class="sxs-lookup"><span data-stu-id="42338-118">**CertCloseStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

<span data-ttu-id="42338-119">此範例會使用 [**MyHandleError**](myhandleerror.md) ，以在發生任何失敗時正常結束程式。</span><span class="sxs-lookup"><span data-stu-id="42338-119">This example uses [**MyHandleError**](myhandleerror.md) to exit the program gracefully in case of any failure.</span></span> <span data-ttu-id="42338-120">程式碼 **MyHandleError** 包含在範例中，也可以在 [一般目的](general-purpose-functions.md)函式下與其他輔助函式一起找到。</span><span class="sxs-lookup"><span data-stu-id="42338-120">The code **MyHandleError** is included with the sample and can also be found along with other auxiliary functions under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Example C Program: 
// Reads a signed and encrypted message, then decrypts and verifies 
// the message.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

BYTE* DecryptAndVerify(DWORD cbBlob, BYTE *pbBlob)
{
    //---------------------------------------------------------------
    //  Declare and initialize local variables.

    HCERTSTORE hCertStore;
    CRYPT_DECRYPT_MESSAGE_PARA DecryptPara;
    CRYPT_VERIFY_MESSAGE_PARA VerifyPara;
    DWORD dwSignerIndex = 0;
    BYTE *pbDecrypted;
    DWORD cbDecrypted;

    //---------------------------------------------------------------
    //   Open the certificate store.

    if ( !(hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    //   Initialize the needed data structures.

    DecryptPara.cbSize = sizeof(CRYPT_DECRYPT_MESSAGE_PARA);
    DecryptPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    DecryptPara.cCertStore = 1;
    DecryptPara.rghCertStore = &hCertStore;

    VerifyPara.cbSize = sizeof(CRYPT_VERIFY_MESSAGE_PARA);
    VerifyPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    VerifyPara.hCryptProv = 0;
    VerifyPara.pfnGetSignerCertificate = NULL;
    VerifyPara.pvGetArg = NULL;
    pbDecrypted = NULL;
    cbDecrypted = 0;

    //---------------------------------------------------------------
    //     Call CryptDecryptAndVerifyMessageSignature a first time
    //     to determine the needed size of the buffer to hold the 
    //     decrypted message. 
    //     Note: The sixth parameter is NULL in this call to 
    //     get the required size of the bytes string to contain the 
    //     decrypted message.

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbBlob,
        cbBlob,
        NULL,           
        &cbDecrypted,
        NULL,
        NULL)))
    {
        MyHandleError(TEXT("Failed getting size."));
    }

    //---------------------------------------------------------------
    //    Allocate memory for the buffer to hold the decrypted
    //    message.

    if(!(pbDecrypted = (BYTE *)malloc(cbDecrypted)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbBlob,
        cbBlob,
        pbDecrypted,
        &cbDecrypted,
        NULL,
        NULL)))
    {
        pbDecrypted = NULL;
    }

    //---------------------------------------------------------------
    //  Close the certificate store.

    CertCloseStore(hCertStore, 0);

    //---------------------------------------------------------------
    //    Return the decrypted string or NULL.

    return pbDecrypted;

} // End of DecryptandVerify.

BYTE* ReadBlob(DWORD *pcbBlob)
{
    FILE *hInputFile;
    BYTE *pbBlob;

    // Open the input file and read in the signed and encrypted BLOB.
    // This file would be created by a program such as the example 
    // program "Example C Program: Sending and Receiving a Signed and 
    // Encrypted Message" in the Platform Software Development Kit (SDK).
    // Change the path name for this file if it is not in the same
    // directory as the executable.

    if( !(hInputFile= _tfopen(TEXT("sandvout.txt"), TEXT("rb"))))
    {
        MyHandleError(TEXT("Input file was not opened.\n"));
    }

    fread(
        pcbBlob,
        sizeof(DWORD),
        1,
        hInputFile);

    if(ferror(hInputFile))
    {
        MyHandleError(TEXT("The size of the BLOB was not read.\n"));
    }

    if(!(pbBlob = (BYTE *) malloc(*pcbBlob)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    fread(
        pbBlob,
        *pcbBlob,
        1,
        hInputFile);

    if(ferror(hInputFile))
    {
        MyHandleError(TEXT("The bytes of the BLOB were not read.\n"));
    }

    fclose(hInputFile);

    return pbBlob;
}  // End of ReadBlob.

//-------------------------------------------------------------------
//   Main calls ReadBlob to read in the signed and encrypted message.
//   It then calls DecryptAndVerify which, if successful, decrypts
//   and verifies the message. 
//   The function main prints the returned, decrypted message
//   if the verification and decryption are successful.

//   Note: The file with the signed and encrypted file must be
//   available, and the user running this program must have access to
//   the private key of the intended message receiver.

//   Also note that this program does not use CryptAcquireContext.
   
void main()
{
    BYTE *pReturnMessage;
    BYTE *pbBlob;
    DWORD cbBlob;

    if((pbBlob = ReadBlob(&cbBlob)) == NULL)
    {
        MyHandleError(TEXT("Read BLOB did not return the BLOB. "));
    }

    if(pReturnMessage = DecryptAndVerify(cbBlob, pbBlob))
    {
        _tprintf(TEXT
                ("    The returned, verified message is ->\n%s\n"), 
            pReturnMessage);
        _tprintf(TEXT("    The program executed without error.\n"));
    }
    else
    {
        _tprintf(TEXT("Verification failed.\n"));
    }

} // End of main.


```



 

 
