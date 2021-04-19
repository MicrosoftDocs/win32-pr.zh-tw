---
description: 說明如何手動驗證安全通道認證。
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: 手動驗證 Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998142"
---
# <a name="manually-validating-schannel-credentials"></a><span data-ttu-id="56d59-103">手動驗證 Schannel 認證</span><span class="sxs-lookup"><span data-stu-id="56d59-103">Manually Validating Schannel Credentials</span></span>

<span data-ttu-id="56d59-104">根據預設，Schannel 會藉由呼叫 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)函數來驗證 [*伺服器憑證*](../secgloss/s-gly.md);但是，如果您已使用「ISC 要求手動認證驗證」旗標來停用這項功能 \_ \_ \_ \_ ，就必須驗證嘗試建立其身分識別的伺服器所提供的憑證。</span><span class="sxs-lookup"><span data-stu-id="56d59-104">By default, Schannel validates the [*server certificate*](../secgloss/s-gly.md) by calling the [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) function; however, if you have disabled this feature using the ISC\_REQ\_MANUAL\_CRED\_VALIDATION flag, you must validate the certificate provided by the server that is attempting to establish its identity.</span></span>

<span data-ttu-id="56d59-105">若要手動驗證伺服器憑證，您必須先取得伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="56d59-105">To manually validate the server certificate, you must first get it.</span></span> <span data-ttu-id="56d59-106">使用 [**QueryCoNtextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) 函數，並指定 SECPKG \_ ATTR \_ REMOTE \_ CERT \_ CONTEXT 屬性值。</span><span class="sxs-lookup"><span data-stu-id="56d59-106">Use the [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) function and specify the SECPKG\_ATTR\_REMOTE\_CERT\_CONTEXT attribute value.</span></span> <span data-ttu-id="56d59-107">這個屬性會傳回 [**憑證 \_ 內容**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) 結構，其中包含伺服器所提供的憑證。</span><span class="sxs-lookup"><span data-stu-id="56d59-107">This attribute returns a [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure containing the certificate supplied by the server.</span></span> <span data-ttu-id="56d59-108">此憑證稱為分葉憑證，因為它是憑證鏈中的最後一個憑證，而且離 [*跟憑證*](../secgloss/r-gly.md)的距離最遠。</span><span class="sxs-lookup"><span data-stu-id="56d59-108">This certificate is called the leaf certificate because it is the last certificate in the certificate chain and is farthest away from the [*root certificate*](../secgloss/r-gly.md).</span></span>

<span data-ttu-id="56d59-109">使用分葉憑證時，您必須確認下列各項：</span><span class="sxs-lookup"><span data-stu-id="56d59-109">Using the leaf certificate you must verify the following:</span></span>

-   <span data-ttu-id="56d59-110">憑證鏈已完成，根是信任的 [*憑證授權單位*](../secgloss/c-gly.md) 單位的憑證 (CA) 。</span><span class="sxs-lookup"><span data-stu-id="56d59-110">The certificate chain is complete and the root is a certificate from a trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="56d59-111">目前的時間不超過憑證鏈中每個憑證的開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="56d59-111">The current time is not beyond the begin and end dates for each of the certificates in the certificate chain.</span></span>
-   <span data-ttu-id="56d59-112">憑證鏈中的憑證都沒有被撤銷。</span><span class="sxs-lookup"><span data-stu-id="56d59-112">None of the certificates in the certificate chain have been revoked.</span></span>
-   <span data-ttu-id="56d59-113">分葉憑證的深度不會比憑證延伸中指定的最大允許深度更深入。</span><span class="sxs-lookup"><span data-stu-id="56d59-113">The depth of the leaf certificate is not deeper than the maximum allowable depth specified in the certificate extension.</span></span> <span data-ttu-id="56d59-114">只有當指定了深度時，才需要進行這項檢查。</span><span class="sxs-lookup"><span data-stu-id="56d59-114">This check is only necessary if there is a depth specified.</span></span>
-   <span data-ttu-id="56d59-115">憑證的使用方式正確，例如，不應該使用 [*用戶端憑證*](../secgloss/c-gly.md) 來驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="56d59-115">The usage of the certificate is correct, for example, a [*client certificate*](../secgloss/c-gly.md) should not be used to authenticate a server.</span></span>
-   <span data-ttu-id="56d59-116">針對伺服器驗證，包含在伺服器之分葉憑證中的伺服器身分識別，與用戶端嘗試聯絡的伺服器相符。</span><span class="sxs-lookup"><span data-stu-id="56d59-116">For server authentication, the server identity contained in the server's leaf certificate matches the server that the client is attempting to contact.</span></span> <span data-ttu-id="56d59-117">一般而言，用戶端會將憑證的 [主體名稱] 欄位中的某個專案與伺服器的 IP 位址或 DNS 名稱進行比對。</span><span class="sxs-lookup"><span data-stu-id="56d59-117">Typically, the client will match some item in the certificate's Subject Name field to the server's IP address or DNS name.</span></span>

 

 
