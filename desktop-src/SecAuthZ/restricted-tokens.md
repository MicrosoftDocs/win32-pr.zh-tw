---
description: 受限的權杖是 CreateRestrictedToken 函式已修改的主要或模擬存取權杖。
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: 受限的權杖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee8e6c89915e3edd0a9206f84a0d3d5697a3cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113796"
---
# <a name="restricted-tokens"></a><span data-ttu-id="a306c-103">受限的權杖</span><span class="sxs-lookup"><span data-stu-id="a306c-103">Restricted Tokens</span></span>

<span data-ttu-id="a306c-104">受限的權杖是 [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)函式已修改的 [*主要*](/windows/desktop/SecGloss/p-gly)或模擬 [*存取權杖*](/windows/desktop/SecGloss/a-gly)。</span><span class="sxs-lookup"><span data-stu-id="a306c-104">A restricted token is a [*primary*](/windows/desktop/SecGloss/p-gly) or impersonation [*access token*](/windows/desktop/SecGloss/a-gly) that has been modified by the [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span> <span data-ttu-id="a306c-105">在受限權杖的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中執行的 [*處理*](/windows/desktop/SecGloss/p-gly)程式或模擬執行緒，其存取安全物件或執行特殊許可權作業的能力會受到限制。</span><span class="sxs-lookup"><span data-stu-id="a306c-105">A [*process*](/windows/desktop/SecGloss/p-gly) or impersonating thread running in the [*security context*](/windows/desktop/SecGloss/s-gly) of a restricted token is restricted in its ability to access securable objects or perform privileged operations.</span></span> <span data-ttu-id="a306c-106">**CreateRestrictedToken** 函式可透過下列方式限制權杖：</span><span class="sxs-lookup"><span data-stu-id="a306c-106">The **CreateRestrictedToken** function can restrict a token in the following ways:</span></span>

-   <span data-ttu-id="a306c-107">移除權杖中的 [許可權](privileges.md) 。</span><span class="sxs-lookup"><span data-stu-id="a306c-107">Remove [privileges](privileges.md) from the token.</span></span>
-   <span data-ttu-id="a306c-108">將僅限拒絕的屬性套用至權杖中的 Sid，讓它們無法用來存取受保護的物件。</span><span class="sxs-lookup"><span data-stu-id="a306c-108">Apply the deny-only attribute to SIDs in the token so that they cannot be used to access secured objects.</span></span> <span data-ttu-id="a306c-109">如需有關僅限拒絕屬性的詳細資訊，請參閱 [存取權杖中的 SID 屬性](sid-attributes-in-an-access-token.md)。</span><span class="sxs-lookup"><span data-stu-id="a306c-109">For more information about the deny-only attribute, see [SID Attributes in an Access Token](sid-attributes-in-an-access-token.md).</span></span>
-   <span data-ttu-id="a306c-110">指定限制 Sid 的清單，這會限制對安全物件的存取。</span><span class="sxs-lookup"><span data-stu-id="a306c-110">Specify a list of restricting SIDs, which can limit access to securable objects.</span></span>

<span data-ttu-id="a306c-111">當系統檢查安全物件的權杖存取權時，系統會使用限制 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="a306c-111">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="a306c-112">當受限制的進程或執行緒嘗試存取安全物件時，系統會執行兩項存取檢查：一個使用權杖啟用的 Sid，另一個使用限制 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="a306c-112">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="a306c-113">只有在這兩個存取檢查都允許要求的存取權限時，才會授與存取權。</span><span class="sxs-lookup"><span data-stu-id="a306c-113">Access is granted only if both access checks allow the requested access rights.</span></span> <span data-ttu-id="a306c-114">如需有關存取檢查的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="a306c-114">For more information about access checks, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="a306c-115">在 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)函式的呼叫中，您可以使用受限制的 [*主要權杖*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="a306c-115">You can use a restricted [*primary token*](/windows/desktop/SecGloss/p-gly) in a call to the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="a306c-116">一般而言，呼叫 **CreateProcessAsUser** 的程式必須擁有 SE \_ ASSIGNPRIMARYTOKEN \_ NAME 許可權，這通常只會由系統程式碼或在 LocalSystem 帳戶中執行的服務所保存。</span><span class="sxs-lookup"><span data-stu-id="a306c-116">Typically, the process that calls **CreateProcessAsUser** must have the SE\_ASSIGNPRIMARYTOKEN\_NAME privilege, which is usually held only by system code or by services running in the LocalSystem account.</span></span> <span data-ttu-id="a306c-117">但是，如果 **CreateProcessAsUser** 呼叫指定受限制版本的呼叫端主要權杖，則不需要此許可權。</span><span class="sxs-lookup"><span data-stu-id="a306c-117">However, if the **CreateProcessAsUser** call specifies a restricted version of the caller's primary token, this privilege is not required.</span></span> <span data-ttu-id="a306c-118">這可讓一般的應用程式建立受限的進程。</span><span class="sxs-lookup"><span data-stu-id="a306c-118">This enables ordinary applications to create restricted processes.</span></span>

<span data-ttu-id="a306c-119">您也可以在 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)函數中使用受限制的主要或模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。</span><span class="sxs-lookup"><span data-stu-id="a306c-119">You can also use a restricted primary or [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="a306c-120">若要判斷權杖是否有限制 Sid 的清單，請呼叫 [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) 函數。</span><span class="sxs-lookup"><span data-stu-id="a306c-120">To determine whether a token has a list of restricting SIDs, call the [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) function.</span></span>

> [!Note]  
> <span data-ttu-id="a306c-121">使用受限制權杖的應用程式應該在預設桌面以外的桌上型電腦上執行受限制的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a306c-121">Applications that use restricted tokens should run the restricted application on desktops other than the default desktop.</span></span> <span data-ttu-id="a306c-122">這是為了避免受限制的應用程式（使用 **SendMessage** 或 **PostMessage**）在預設桌上型電腦上不受限制的應用程式所造成的攻擊。</span><span class="sxs-lookup"><span data-stu-id="a306c-122">This is necessary to prevent an attack by a restricted application, using **SendMessage** or **PostMessage**, to unrestricted applications on the default desktop.</span></span> <span data-ttu-id="a306c-123">如有必要，請在桌上型電腦之間切換，以進行應用程式用途。</span><span class="sxs-lookup"><span data-stu-id="a306c-123">If necessary, switch between desktops for your application purposes.</span></span>

 

 

 
