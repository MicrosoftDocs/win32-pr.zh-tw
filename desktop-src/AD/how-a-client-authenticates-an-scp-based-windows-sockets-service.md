---
title: 用戶端如何驗證 SCP 型 Windows 通訊端服務
description: 本主題顯示用戶端應用程式用來撰寫服務之 SPN 的程式碼。
ms.assetid: b5ef79c6-e321-435c-b3de-817fdea8836a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38471f48d8c80d0795b7176b95df0029d42325ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462020"
---
# <a name="how-a-client-authenticates-an-scp-based-windows-sockets-service"></a><span data-ttu-id="90115-103">用戶端如何驗證 SCP 型 Windows 通訊端服務</span><span class="sxs-lookup"><span data-stu-id="90115-103">How a Client Authenticates an SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="90115-104">本主題顯示用戶端應用程式用來撰寫服務之 SPN 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="90115-104">This topic shows the code that a client application uses to compose an SPN for a service.</span></span> <span data-ttu-id="90115-105">用戶端會系結至服務的服務連接點 (SCP) 來取得連接到服務所需的資料。</span><span class="sxs-lookup"><span data-stu-id="90115-105">The client binds to the service's service connection point (SCP) to retrieve the data required to connect to the service.</span></span> <span data-ttu-id="90115-106">SCP 也包含用戶端可以用來撰寫服務 SPN 的資料。</span><span class="sxs-lookup"><span data-stu-id="90115-106">The SCP also contains data that the client can use to compose the service's SPN.</span></span> <span data-ttu-id="90115-107">如需系結至 SCP 並抓取必要屬性的詳細資訊和程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="90115-107">For more information and a code example that binds to the SCP and retrieves the necessary properties, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="90115-108">本主題也會示範用戶端如何使用 SSPI 安全性封裝和服務的 SPN 來建立與 Windows 通訊端服務的相互驗證連線。</span><span class="sxs-lookup"><span data-stu-id="90115-108">This topic also shows how a client uses an SSPI security package and the service's SPN to establish a mutually authenticated connection to the Windows Sockets service.</span></span> <span data-ttu-id="90115-109">請注意，此程式碼與 Microsoft Windows NT 4.0 及更早版本中所需的程式碼幾乎完全相同，只是向伺服器驗證用戶端。</span><span class="sxs-lookup"><span data-stu-id="90115-109">Be aware that this code is almost identical to the code required in Microsoft Windows NT 4.0 and earlier just to authenticate the client to the server.</span></span> <span data-ttu-id="90115-110">唯一的差別在於用戶端必須提供 SPN，並指定 ISC 要求的 \_ \_ 相互 \_ 驗證旗標。</span><span class="sxs-lookup"><span data-stu-id="90115-110">The only difference is that the client must supply the SPN and specify the ISC\_REQ\_MUTUAL\_AUTH flag.</span></span>

## <a name="client-code-to-make-an-spn-for-a-service"></a><span data-ttu-id="90115-111">用來建立服務 SPN 的用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="90115-111">Client Code to Make an SPN for a Service</span></span>


```C++
// Initialize these strings by querying the service's SCP.
TCHAR szDn[MAX_PATH],     // DN of the service's SCP.
      szServer[MAX_PATH], // DNS name of the service's server.
      szClass[MAX_PATH];  // Service class.
 
TCHAR szSpn[MAX_PATH];    // Buffer for SPN.
SOCKET sockServer;        // Socket connected to service.
DWORD dwRes, dwLen;
.
.
.
// Compose the SPN for the service using the DN, Class, and Server
// returned by ScpLocate.
dwLen = sizeof(szSpn);
dwRes = DsMakeSpn(
     szClass,    // Service class.
     szDn,       // DN of the service's SCP.
     szServer,   // DNS name of the server on which service is running.
     0,          // No port component in SPN.
     NULL,       // No referrer.
     &dwLen,     // Size of szSpn buffer.
     szSpn);     // Buffer to receive the SPN.

if (!DoAuthentication (sockServer, szSpn)) {
    closesocket (sockServer);
    return(FALSE);
}
.
.
.
```



## <a name="client-code-to-authenticate-the-service"></a><span data-ttu-id="90115-112">用來驗證服務的用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="90115-112">Client Code to Authenticate the Service</span></span>

<span data-ttu-id="90115-113">這個程式碼範例是由兩個常式組成： **DoAuthentication** 和 **GenClientCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="90115-113">This code example consists of two routines: **DoAuthentication** and **GenClientContext**.</span></span> <span data-ttu-id="90115-114">在呼叫 [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) 來撰寫服務的 spn 之後，用戶端會將 spn 傳遞給 **DoAuthentication** 常式，其會呼叫 **GenClientCoNtext** 來產生要傳送至服務的初始緩衝區。</span><span class="sxs-lookup"><span data-stu-id="90115-114">After calling [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) to compose an SPN for the service, the client passes the SPN to the **DoAuthentication** routine, which calls the **GenClientContext** to generate the initial buffer to send to the service.</span></span> <span data-ttu-id="90115-115">**DoAuthentication** 會使用通訊端控制碼來傳送緩衝區，並藉由另一個對 **GenClientCoNtext** 的呼叫來接收傳遞給 SSPI 封裝的服務回應。</span><span class="sxs-lookup"><span data-stu-id="90115-115">**DoAuthentication** uses the socket handle to send the buffer and receive the service's response passed to the SSPI package by another call to **GenClientContext**.</span></span> <span data-ttu-id="90115-116">此迴圈會重複，直到驗證失敗或 **GenClientCoNtext** 設定指出驗證成功的旗標。</span><span class="sxs-lookup"><span data-stu-id="90115-116">This loop is repeated until the authentication fails or **GenClientContext** sets a flag that indicates the authentication succeeded.</span></span>

<span data-ttu-id="90115-117">**GenClientCoNtext** 常式會與 SSPI 套件互動，以產生要傳送至服務的驗證資料，以及處理從服務收到的資料。</span><span class="sxs-lookup"><span data-stu-id="90115-117">The **GenClientContext** routine interacts with the SSPI package to generate the authentication data to send to the service and process the data received from the service.</span></span> <span data-ttu-id="90115-118">用戶端所提供之驗證資料的重要元件包括：</span><span class="sxs-lookup"><span data-stu-id="90115-118">The key components of the authentication data provided by the client include:</span></span>

-   <span data-ttu-id="90115-119">用來識別服務必須驗證之認證的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="90115-119">The service principal name which identifies the credentials that the service must authenticate.</span></span>
-   <span data-ttu-id="90115-120">用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="90115-120">The client's credentials.</span></span> <span data-ttu-id="90115-121">安全性套件的 [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) 函式會從登入時建立的用戶端安全性內容中，解壓縮這些認證。</span><span class="sxs-lookup"><span data-stu-id="90115-121">The [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) function of the security package extracts these credentials from the client's security context established at logon.</span></span>
-   <span data-ttu-id="90115-122">若要要求相互驗證，用戶端必須在 \_ \_ \_ **GenClientCoNtext** 常式期間呼叫 [**INITIALIZESECURITYCONTEXT**](../SecAuthN/initializesecuritycontext--general.md)函式時，指定 ISC 要求的相互驗證旗標。</span><span class="sxs-lookup"><span data-stu-id="90115-122">To request mutual authentication, the client must specify the ISC\_REQ\_MUTUAL\_AUTH flag when it calls the [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) function during the **GenClientContext** routine.</span></span>


```C++
// Structure for storing the state of the authentication sequence.
typedef struct _AUTH_SEQ 
{
    BOOL _fNewConversation;
    CredHandle _hcred;
    BOOL _fHaveCredHandle;
    BOOL _fHaveCtxtHandle;
    struct _SecHandle  _hctxt;
} AUTH_SEQ, *PAUTH_SEQ;
 
/***************************************************************/
//   DoAuthentication routine for the client.
//
//   Manages the client's authentication conversation with the service 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL DoAuthentication (
        SOCKET s, 
        LPTSTR szSpn)
{
BOOL done = FALSE;
DWORD cbOut, cbIn;
 
// Call the security package to generate the initial buffer of 
// authentication data to send to the service.
cbOut = g_cbMaxMessage;
if (!GenClientContext (s, NULL, 0, g_pOutBuf, 
                       &cbOut, &done, szSpn))
    return(FALSE);
    
if (!SendMsg (s, g_pOutBuf, cbOut))
    return(FALSE);
 
// Pass the service's response back to the security package, and send 
// the package's output back to the service. Repeat until complete.
while (!done) 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenClientContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                           &cbOut, &done, szSpn))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
}
 
return(TRUE);
}
 
/***************************************************************/
//   GenClientContext routine
//
//   Handles the client's interactions with the security package.
//   Optionally takes an input buffer coming from the service 
//   and generates a buffer of data to send back to the 
//   service. Also returns an indication when the authentication
//   is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenClientContext (
            DWORD dwKey,     // Socket handle used as key.
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone,
            LPTSTR szSpn)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes;
PAUTH_SEQ        pAS; // Structure to store state of authentication.
 
// Get structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
            NULL,    // Principal
            PACKAGE_NAME,
            SECPKG_CRED_OUTBOUND,
            NULL,    // LOGON id
            NULL,    // Authentication data
            NULL,    // Get key function.
            NULL,    // Get key argument.
            &pAS->_hcred,
            &Lifetime
            );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else 
    {
        fprintf (stderr, 
                 "AcquireCredentialsHandle failed: %u\n", ssStatus);
        return(FALSE);
    }
}
 
// Prepare output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers = 1;
OutBuffDesc.pBuffers = &OutSecBuff;
 
OutSecBuff.cbBuffer = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer = pOut;
 
// Prepare input buffer.
if (!pAS->_fNewConversation) 
{
    InBuffDesc.ulVersion = 0;
    InBuffDesc.cBuffers = 1;
    InBuffDesc.pBuffers = &InSecBuff;
 
    InSecBuff.cbBuffer = cbIn;
    InSecBuff.BufferType = SECBUFFER_TOKEN;
    InSecBuff.pvBuffer = pIn;
}
 
_tprintf(TEXT("InitializeSecurityContext: pszTarget=%s\n"),szSpn);
 
ssStatus = g_pFuncs->InitializeSecurityContext (
                     &pAS->_hcred,
                     pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                     szSpn,
                     ISC_REQ_MUTUAL_AUTH,      // Context requirements
                     0,                        // Reserved1
                     SECURITY_NATIVE_DREP,
                     pAS->_fNewConversation ? NULL : &InBuffDesc,
                     0,                        // Reserved2
                     &pAS->_hctxt,
                     &OutBuffDesc,
                     &ContextAttributes,
                     &Lifetime
                     );
if (!SEC_SUCCESS (ssStatus)) 
{
    fprintf (stderr, "init context failed: %X\n", ssStatus);
    return FALSE;
}
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete token if applicable.
if ( (SEC_I_COMPLETE_NEEDED == ssStatus) || 
     (SEC_I_COMPLETE_AND_CONTINUE == ssStatus))  
{
    if (g_pFuncs->CompleteAuthToken) 
    {
        ssStatus = g_pFuncs->CompleteAuthToken (&pAS->_hctxt, 
                                                &OutBuffDesc);
        if (!SEC_SUCCESS(ssStatus)) 
        {
            fprintf (stderr, "complete failed: %u\n", ssStatus);
            return FALSE;
        }
    } else 
    {
        fprintf (stderr, "Complete not supported.\n");
        return FALSE;
    }
}
 
*pcbOut = OutSecBuff.cbBuffer;
 
if (pAS->_fNewConversation)
    pAS->_fNewConversation = FALSE;
 
*pfDone = !((SEC_I_CONTINUE_NEEDED == ssStatus) ||
            (SEC_I_COMPLETE_AND_CONTINUE == ssStatus));
 
// Check the ISC_RET_MUTUAL_AUTH flag to verify that 
// mutual authentication was performed.
if (*pfDone && !(ContextAttributes && ISC_RET_MUTUAL_AUTH) )
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
return TRUE;
}
```



 

 




