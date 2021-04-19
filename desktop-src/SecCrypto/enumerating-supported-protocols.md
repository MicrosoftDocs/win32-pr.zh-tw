---
description: 您可以呼叫 CryptGetProvParam 搭配 PP \_ ENUMALGS 或 pp ENUMALGS 範例來列出支援的通訊協定和加密套件 \_ \_ 。
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: 列舉支援的通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971745"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="8863f-103">列舉支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="8863f-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="8863f-104">您可以呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) 搭配 pp \_ ENUMALGS 或 pp ENUMALGS 範例來列出支援的通訊協定和加密套件 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8863f-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="8863f-105">PP \_ ENUMALGS \_ ex 值的運作方式類似 PP \_ ENUMALGS，但會傳回 [**>prov \_ ENUMALGS \_ EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) 結構，以保存提供者所支援之演算法的更廣泛資訊。</span><span class="sxs-lookup"><span data-stu-id="8863f-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="8863f-106">如需定義的通訊協定旗標及其值的詳細資訊，請參閱 [通訊協定旗標](protocol-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="8863f-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="8863f-107">假設 **hCryptProv** 成員是使用 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)取得的開放式密碼編譯 [*內容*](../secgloss/c-gly.md)[*控制碼*](../secgloss/h-gly.md)，並將其 *dwProvType* 參數設定為 >prov \_ RSA \_ SCHANNEL，則下列範例會列出 CSP 中所有可用的演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="8863f-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



<span data-ttu-id="8863f-108">下表列出一般國內 >PROV RSA 安全通道 CSP 所傳回的一些演算法 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8863f-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="8863f-109">請注意，此範例中的 CSP 不支援 SSL2 SHA Mac 或 SSL2 DES encryption。</span><span class="sxs-lookup"><span data-stu-id="8863f-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="8863f-110">演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="8863f-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="8863f-111">最小金鑰長度</span><span class="sxs-lookup"><span data-stu-id="8863f-111">Minimum key length</span></span> | <span data-ttu-id="8863f-112">最大金鑰長度</span><span class="sxs-lookup"><span data-stu-id="8863f-112">Maximum key length</span></span> | <span data-ttu-id="8863f-113">通訊協定</span><span class="sxs-lookup"><span data-stu-id="8863f-113">Protocols</span></span> | <span data-ttu-id="8863f-114">演算法名稱</span><span class="sxs-lookup"><span data-stu-id="8863f-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="8863f-115">*CALG \_ RSA \_ KEYX*</span><span class="sxs-lookup"><span data-stu-id="8863f-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="8863f-116">512</span><span class="sxs-lookup"><span data-stu-id="8863f-116">512</span></span>                | <span data-ttu-id="8863f-117">2048</span><span class="sxs-lookup"><span data-stu-id="8863f-117">2048</span></span>               | <span data-ttu-id="8863f-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="8863f-118">0x0007</span></span>    | <span data-ttu-id="8863f-119">"RSA \_ KEYX"</span><span class="sxs-lookup"><span data-stu-id="8863f-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="8863f-120">*CALG \_ MD5*</span><span class="sxs-lookup"><span data-stu-id="8863f-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="8863f-121">128</span><span class="sxs-lookup"><span data-stu-id="8863f-121">128</span></span>                | <span data-ttu-id="8863f-122">128</span><span class="sxs-lookup"><span data-stu-id="8863f-122">128</span></span>                | <span data-ttu-id="8863f-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="8863f-123">0x0007</span></span>    | <span data-ttu-id="8863f-124">MD5</span><span class="sxs-lookup"><span data-stu-id="8863f-124">"MD5"</span></span>          |
| [<span data-ttu-id="8863f-125">*CALG \_ SHA*</span><span class="sxs-lookup"><span data-stu-id="8863f-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="8863f-126">160</span><span class="sxs-lookup"><span data-stu-id="8863f-126">160</span></span>                | <span data-ttu-id="8863f-127">160</span><span class="sxs-lookup"><span data-stu-id="8863f-127">160</span></span>                | <span data-ttu-id="8863f-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="8863f-128">0x0005</span></span>    | <span data-ttu-id="8863f-129">SHA</span><span class="sxs-lookup"><span data-stu-id="8863f-129">"SHA"</span></span>          |
| [<span data-ttu-id="8863f-130">*CALG \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="8863f-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="8863f-131">40</span><span class="sxs-lookup"><span data-stu-id="8863f-131">40</span></span>                 | <span data-ttu-id="8863f-132">128</span><span class="sxs-lookup"><span data-stu-id="8863f-132">128</span></span>                | <span data-ttu-id="8863f-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="8863f-133">0x0007</span></span>    | <span data-ttu-id="8863f-134">RC4</span><span class="sxs-lookup"><span data-stu-id="8863f-134">"RC4"</span></span>          |
| <span data-ttu-id="8863f-135">CALG \_ DES</span><span class="sxs-lookup"><span data-stu-id="8863f-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="8863f-136">56</span><span class="sxs-lookup"><span data-stu-id="8863f-136">56</span></span>                 | <span data-ttu-id="8863f-137">56</span><span class="sxs-lookup"><span data-stu-id="8863f-137">56</span></span>                 | <span data-ttu-id="8863f-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="8863f-138">0x0005</span></span>    | <span data-ttu-id="8863f-139">演算法</span><span class="sxs-lookup"><span data-stu-id="8863f-139">"DES"</span></span>          |



 

<span data-ttu-id="8863f-140">為了準備傳送 ClientHello 或傳回 serverhello 訊息， [*Schannel*](../secgloss/s-gly.md) 通訊協定引擎會列舉 CSP 所支援的演算法和金鑰大小，並在內部建立支援的加密套件清單。</span><span class="sxs-lookup"><span data-stu-id="8863f-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
