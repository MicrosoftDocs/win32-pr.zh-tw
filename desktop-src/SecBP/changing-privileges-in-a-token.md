---
description: 說明如何使用 AdjustTokenPrivileges 和 CreateRestrictedToken 函數來變更權杖中的許可權。
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: 變更權杖中的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975898"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="98ca2-103">變更權杖中的許可權</span><span class="sxs-lookup"><span data-stu-id="98ca2-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="98ca2-104">您可以透過兩種方式來變更主要或模擬權杖中的許可權：</span><span class="sxs-lookup"><span data-stu-id="98ca2-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="98ca2-105">使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數來啟用或停用許可權。</span><span class="sxs-lookup"><span data-stu-id="98ca2-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="98ca2-106">使用 [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) 函數來限制或移除許可權。</span><span class="sxs-lookup"><span data-stu-id="98ca2-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="98ca2-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 無法新增或移除權杖中的許可權。</span><span class="sxs-lookup"><span data-stu-id="98ca2-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="98ca2-108">它只能啟用目前停用的現有許可權，或停用目前已啟用的現有許可權。</span><span class="sxs-lookup"><span data-stu-id="98ca2-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="98ca2-109">如需範例，請參閱 [啟用和停用 c + + 中的許可權](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="98ca2-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="98ca2-110">若要將許可權指派給使用者帳戶，請參閱將 [許可權指派給帳戶](assigning-privileges-to-an-account.md)。</span><span class="sxs-lookup"><span data-stu-id="98ca2-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="98ca2-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) 具有更廣泛的功能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="98ca2-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="98ca2-112">移除許可權。</span><span class="sxs-lookup"><span data-stu-id="98ca2-112">Removing a privilege.</span></span> <span data-ttu-id="98ca2-113">請注意，移除許可權與停用許可權不同。</span><span class="sxs-lookup"><span data-stu-id="98ca2-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="98ca2-114">從權杖移除許可權之後，就無法將它放回。</span><span class="sxs-lookup"><span data-stu-id="98ca2-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="98ca2-115">將拒絕屬性附加至權杖中的 Sid。</span><span class="sxs-lookup"><span data-stu-id="98ca2-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="98ca2-116">這會造成不允許特定群組或帳戶的影響，例如拒絕 Everyone 群組刪除特定檔案的存取權。</span><span class="sxs-lookup"><span data-stu-id="98ca2-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="98ca2-117">如需限制 Sid 的詳細資訊，請參閱 [存取權杖中的 SID 屬性](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token)。</span><span class="sxs-lookup"><span data-stu-id="98ca2-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="98ca2-118">指定限制權杖中 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="98ca2-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="98ca2-119">如需限制 Sid 的詳細資訊，請參閱 [限制的權杖](/windows/desktop/SecAuthZ/restricted-tokens)。</span><span class="sxs-lookup"><span data-stu-id="98ca2-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
