---
description: 下列函式是可以擴充的 CryptoAPI 函數之一。
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: 建立新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511174"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="71d68-103">建立新功能</span><span class="sxs-lookup"><span data-stu-id="71d68-103">Creating the New Functionality</span></span>

<span data-ttu-id="71d68-104">下列函式是可以擴充的 CryptoAPI 函數之一。</span><span class="sxs-lookup"><span data-stu-id="71d68-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="71d68-105">CryptoAPI 函數</span><span class="sxs-lookup"><span data-stu-id="71d68-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="71d68-106">OID 函數名稱定義</span><span class="sxs-lookup"><span data-stu-id="71d68-106">OID function name define</span></span>                         | <span data-ttu-id="71d68-107">OID 函數名稱字串</span><span class="sxs-lookup"><span data-stu-id="71d68-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="71d68-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="71d68-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="71d68-109">CRYPT \_ OID \_ 編碼 \_ OBJECT \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="71d68-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="71d68-110">"CryptDllEncodeObject"</span><span class="sxs-lookup"><span data-stu-id="71d68-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="71d68-111">**CryptDecodeObject**</span><span class="sxs-lookup"><span data-stu-id="71d68-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="71d68-112">CRYPT \_ OID \_ 解碼 \_ 物件 \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="71d68-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="71d68-113">"CryptDllDecodeObject"</span><span class="sxs-lookup"><span data-stu-id="71d68-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="71d68-114">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="71d68-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="71d68-115">CRYPT \_ OID \_ OPEN \_ STORE \_ >PROV \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="71d68-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="71d68-116">"CertDllOpenStoreProv"</span><span class="sxs-lookup"><span data-stu-id="71d68-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="71d68-117">**CertVerifyCTLUsage**</span><span class="sxs-lookup"><span data-stu-id="71d68-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="71d68-118">CRYPT \_ OID \_ 驗證 \_ CTL \_ 使用方式 \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="71d68-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="71d68-119">"CertDllVerifyCTLUsage"</span><span class="sxs-lookup"><span data-stu-id="71d68-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="71d68-120">**CertVerifyRevocation**</span><span class="sxs-lookup"><span data-stu-id="71d68-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="71d68-121">CRYPT \_ OID \_ 確認 \_ 撤銷 \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="71d68-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="71d68-122">"CertDllVerifyRevocation"</span><span class="sxs-lookup"><span data-stu-id="71d68-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="71d68-123">在一般情況下使用現有的 OID 和編碼類型時，會使用 CryptoAPI 函式本身的程式碼。</span><span class="sxs-lookup"><span data-stu-id="71d68-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="71d68-124">如果使用 OID 函式中的程式碼所呼叫的其中一個函式不是設計來處理的，則必須在 DLL 中建立包含新功能的新函式。</span><span class="sxs-lookup"><span data-stu-id="71d68-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="71d68-125">該 DLL 必須在登錄中註冊或安裝在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="71d68-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="71d68-126">使用新指定的 OID 和編碼類型呼叫其中一個列出的函式時，會使用新 DLL 中的程式碼，而不是 CryptoAPI 函式所提供的程式碼。</span><span class="sxs-lookup"><span data-stu-id="71d68-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="71d68-127">新開發的函式名稱可以是上表的「OID 函式名稱字串」下所列的名稱，或者，在註冊新的函式程式碼時，可以指定不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="71d68-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="71d68-128">新的函數必須使用適當的原型。</span><span class="sxs-lookup"><span data-stu-id="71d68-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="71d68-129">除了 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)以外的所有情況下，這個原型與呼叫 new 函式的 CryptoAPI 函數相同。</span><span class="sxs-lookup"><span data-stu-id="71d68-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="71d68-130">在 **CertOpenStore** 的案例中，原型如下所示。</span><span class="sxs-lookup"><span data-stu-id="71d68-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="71d68-131">如果原型不相符，系統堆疊將會損毀。</span><span class="sxs-lookup"><span data-stu-id="71d68-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="71d68-132">除了提供 DLL 中新函式的程式碼之外，擴充 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 或 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 的功能需要將新 C 資料結構的型別定義放在使用者的程式編譯時所包含的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="71d68-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




