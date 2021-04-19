---
description: 指定 Schannel 密碼和加密的強度
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: 指定 Schannel 密碼和加密的強度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984651"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a><span data-ttu-id="da22e-103">指定 Schannel 密碼和加密的強度</span><span class="sxs-lookup"><span data-stu-id="da22e-103">Specifying Schannel Ciphers and Cipher Strengths</span></span>

<span data-ttu-id="da22e-104">針對用戶端/伺服器資訊交換，Schannel 的預設行為是根據登錄中啟用的密碼來協商可用的最佳加密。</span><span class="sxs-lookup"><span data-stu-id="da22e-104">For client/server information exchanges, the default behavior of Schannel is to negotiate the best cipher available based on those enabled in the registry.</span></span> <span data-ttu-id="da22e-105">應用程式可能會使用安全通道認證結構的成員，限制連接所允許的加密和加密強度， [**如下所示 \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) ：</span><span class="sxs-lookup"><span data-stu-id="da22e-105">Applications may limit the ciphers and cipher strengths allowed for a connection by using members of the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure as follows:</span></span>

1.  <span data-ttu-id="da22e-106">將 **palgSupportedAlgs** 成員設定為包含允許之密碼的 [**ALG \_ 識別碼**](../seccrypto/alg-id.md) 陣列。</span><span class="sxs-lookup"><span data-stu-id="da22e-106">Set the **palgSupportedAlgs** member to an array of [**ALG\_ID**](../seccrypto/alg-id.md) containing the allowable ciphers.</span></span> <span data-ttu-id="da22e-107">如需詳細資訊，請參閱密碼識別碼。</span><span class="sxs-lookup"><span data-stu-id="da22e-107">For more information, see Cipher IDs.</span></span>
2.  <span data-ttu-id="da22e-108">將 **dwMinimumCipherStrength** 和/或 **dwMaximumCipherStrength** 成員設定為允許的最小和最大強度。</span><span class="sxs-lookup"><span data-stu-id="da22e-108">Set the **dwMinimumCipherStrength** and/or **dwMaximumCipherStrength** members to the allowable minimum and maximum strengths.</span></span> <span data-ttu-id="da22e-109">如需詳細資訊，請參閱加密強度值。</span><span class="sxs-lookup"><span data-stu-id="da22e-109">For more information, see Cipher Strength Values.</span></span>
3.  <span data-ttu-id="da22e-110">透過呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函式的 *pAuthData* 參數) [**，將安全通道認證結構 (\_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) 。</span><span class="sxs-lookup"><span data-stu-id="da22e-110">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (by means of the *pAuthData* parameter) in a call to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="da22e-111">此函數會傳回認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="da22e-111">This function returns a credentials handle.</span></span>
4.  <span data-ttu-id="da22e-112">在用戶端 InitializeSecurityCoNtext 的呼叫中指定認證控制碼 [**(一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數或伺服器端 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式。</span><span class="sxs-lookup"><span data-stu-id="da22e-112">Specify the credentials handle in a call to the client-side [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function or the server-side [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

## <a name="cipher-ids"></a><span data-ttu-id="da22e-113">加密識別碼</span><span class="sxs-lookup"><span data-stu-id="da22e-113">Cipher IDs</span></span>

<span data-ttu-id="da22e-114">Schannel 的預設行為是根據系統登錄中的 Schannel 專案要求可用的最佳加密。</span><span class="sxs-lookup"><span data-stu-id="da22e-114">The default behavior of Schannel is to request the best cipher available based on Schannel entries in the system registry.</span></span> <span data-ttu-id="da22e-115">請勿變更系統登錄;它針對 Schannel 所包含的設定會在全域使用，並會影響其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="da22e-115">Do not change the system registry; the settings it contains for Schannel are used globally and will affect other applications.</span></span> <span data-ttu-id="da22e-116">如需有效的常數清單，請參閱 [**ALG \_ 識別碼**](../seccrypto/alg-id.md)。</span><span class="sxs-lookup"><span data-stu-id="da22e-116">For the list of valid constants, see [**ALG\_ID**](../seccrypto/alg-id.md).</span></span>

## <a name="cipher-strength-values"></a><span data-ttu-id="da22e-117">加密強度值</span><span class="sxs-lookup"><span data-stu-id="da22e-117">Cipher Strength Values</span></span>

<span data-ttu-id="da22e-118">這種安全通道功能通常是用來限制與國內或出口強度加密的連接。</span><span class="sxs-lookup"><span data-stu-id="da22e-118">This Schannel feature is typically used to limit a connection to either domestic or export strength ciphers.</span></span> <span data-ttu-id="da22e-119">國內的強項包括56和128位，而匯出強度限制為56位。</span><span class="sxs-lookup"><span data-stu-id="da22e-119">Domestic strengths include 56, and 128 bits, while export strength is limited to 56 bits.</span></span> <span data-ttu-id="da22e-120">如果您將最小值和最大值設定為零，則 Schannel 將會使用所有可用的加密強度。</span><span class="sxs-lookup"><span data-stu-id="da22e-120">If you set the minimum and maximum values to zero Schannel will use all available cipher strengths.</span></span>

<span data-ttu-id="da22e-121">使用 TLS 或 SSL 3.0，將 **dwMinimumCipherStrength** 成員設定為-1 (負一個) 來啟用 "Null cipher" 加密套件，以提供簽章但不加密。</span><span class="sxs-lookup"><span data-stu-id="da22e-121">Using TLS or SSL 3.0, set the **dwMinimumCipherStrength** member to -1 (negative one) to enable the "Null Cipher" cipher suites, which provide signatures but no encryption.</span></span> <span data-ttu-id="da22e-122">如果 **dwMaximumCipherStrength** 也設定為-1，則只會啟用 "Null Cipher" 套件。</span><span class="sxs-lookup"><span data-stu-id="da22e-122">If **dwMaximumCipherStrength** is also set to -1 then only the "Null Cipher" suites will be enabled.</span></span> <span data-ttu-id="da22e-123">這項設定僅供開發之用，不應該用於生產系統。</span><span class="sxs-lookup"><span data-stu-id="da22e-123">This setting is intended for development only and should not be used in production systems.</span></span>

## <a name="querying-cipher-information"></a><span data-ttu-id="da22e-124">查詢加密資訊</span><span class="sxs-lookup"><span data-stu-id="da22e-124">Querying Cipher Information</span></span>

<span data-ttu-id="da22e-125">若要取得認證的加密強度設定，請呼叫 [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) 函式，並 \_ 將 SECPKG ATTR \_ 加密強度指定 \_ 為 *ulAttribute* 參數。</span><span class="sxs-lookup"><span data-stu-id="da22e-125">To retrieve the cipher strength settings for a credential, call the [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function and specify SECPKG\_ATTR\_CIPHER\_STRENGTHS as the *ulAttribute* parameter.</span></span>

<span data-ttu-id="da22e-126">若要取得認證的支援演算法清單，請使用 SECPKG ATTR 支援的 ALGS 來呼叫 [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) ， \_ \_ \_ 作為 *ulAttribute* 參數。</span><span class="sxs-lookup"><span data-stu-id="da22e-126">To retrieve the list of supported algorithms for a credential, call the [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) with SECPKG\_ATTR\_SUPPORTED\_ALGS as the *ulAttribute* parameter.</span></span>

 

 
