---
description: 所有的安全通道通訊協定都需要伺服器提供信任憑證授權單位單位的憑證 (CA) 作為其身分識別的證明。
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: 使用 Schannel 執行驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a37b8dedf07680286288234c7ca4422f44c2c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983517"
---
# <a name="performing-authentication-using-schannel"></a><span data-ttu-id="f1943-103">使用 Schannel 執行驗證</span><span class="sxs-lookup"><span data-stu-id="f1943-103">Performing Authentication Using Schannel</span></span>

<span data-ttu-id="f1943-104">所有的安全通道通訊協定都需要伺服器提供信任 [*憑證授權單位*](../secgloss/c-gly.md)[*單位的憑證*](../secgloss/c-gly.md) (CA) 作為其身分識別的證明。</span><span class="sxs-lookup"><span data-stu-id="f1943-104">All Schannel protocols require the server to provide a [*certificate*](../secgloss/c-gly.md) from a trusted [*certification authority*](../secgloss/c-gly.md) (CA) as proof of its identity.</span></span> <span data-ttu-id="f1943-105">此進程稱為伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="f1943-105">This process is called server authentication.</span></span> <span data-ttu-id="f1943-106">用戶端驗證（用戶端會提供其身分識別的證明）是選擇性的，而且可能隨時由伺服器要求。</span><span class="sxs-lookup"><span data-stu-id="f1943-106">Client authentication, where the client provides proof of its identity, is optional and may be requested by the server at any time.</span></span>

## <a name="authenticating-the-server"></a><span data-ttu-id="f1943-107">驗證服務器</span><span class="sxs-lookup"><span data-stu-id="f1943-107">Authenticating the Server</span></span>

<span data-ttu-id="f1943-108">Schannel 的預設行為是使用 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)函數來驗證 [*伺服器憑證*](../secgloss/s-gly.md)的 [*完整性*](../secgloss/i-gly.md)和擁有權。</span><span class="sxs-lookup"><span data-stu-id="f1943-108">The default behavior of Schannel is to use the [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) function to verify the [*integrity*](../secgloss/i-gly.md) and ownership of the [*server certificate*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f1943-109">若要停用此功能， \_ 請 \_ \_ \_ 在呼叫 [**InitializeSecurityCoNtext (Schannel)**](./initializesecuritycontext--schannel.md) 函式時，指定 ISC 要求手動認證驗證。</span><span class="sxs-lookup"><span data-stu-id="f1943-109">To disable this feature, specify ISC\_REQ\_MANUAL\_CRED\_VALIDATION when calling the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="f1943-110">如需詳細資訊，請參閱 [手動驗證 Schannel 認證](manually-validating-schannel-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="f1943-110">For more information, see [Manually Validating Schannel Credentials](manually-validating-schannel-credentials.md).</span></span>

## <a name="authenticating-the-client"></a><span data-ttu-id="f1943-111">驗證用戶端</span><span class="sxs-lookup"><span data-stu-id="f1943-111">Authenticating the Client</span></span>

<span data-ttu-id="f1943-112">Schannel 不會驗證用戶端的憑證;伺服器必須手動執行此驗證。</span><span class="sxs-lookup"><span data-stu-id="f1943-112">Schannel does not validate client's certificates; the server must perform this authentication manually.</span></span> <span data-ttu-id="f1943-113">一般來說，伺服器會在包含使用者帳戶資訊的資料庫中檢查用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f1943-113">Typically, the server will check the client's identity in a database containing user account information.</span></span> <span data-ttu-id="f1943-114">對於需要使用憑證取得用戶端帳戶的伺服器，請參閱 [對應憑證](mapping-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="f1943-114">For servers that need to obtain a client's account using a certificate, see [Mapping Certificates](mapping-certificates.md).</span></span>

<span data-ttu-id="f1943-115">當伺服器要求用戶端驗證時，用戶端必須將其中一個憑證傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1943-115">When the server requests client authentication, the client must send the server one of its certificates.</span></span> <span data-ttu-id="f1943-116">根據預設，安全通道不會通知用戶端，而是嘗試找出 [*用戶端憑證*](../secgloss/c-gly.md) ，並將它傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1943-116">By default, Schannel will, with no notification to the client, attempt to locate a [*client certificate*](../secgloss/c-gly.md) and send it to the server.</span></span> <span data-ttu-id="f1943-117">若要停用此功能，用戶端會 \_ \_ \_ \_ 在呼叫 [**InitializeSecurityCoNtext (Schannel)**](./initializesecuritycontext--schannel.md) 函式時，指定 ISC 需求使用提供的認證。</span><span class="sxs-lookup"><span data-stu-id="f1943-117">To disable this feature, clients specify ISC\_REQ\_USE\_SUPPLIED\_CREDS when calling the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="f1943-118">當指定這個旗標時， \_ \_ \_ 當伺服器要求驗證，且用戶端先前未提供憑證時，Schannel 會將每秒未完成的認證傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="f1943-118">When this flag is specified, Schannel will return SEC\_I\_INCOMPLETE\_CREDENTIALS to the client when the server requests authentication and the client has not previously supplied a certificate.</span></span>

 

 
