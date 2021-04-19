---
description: 物件擁有者隱含擁有 \_ 物件的寫入 DAC 存取權。 這表示擁有者可以在 (DACL) 的情況下，修改物件的任意存取控制清單，因此可以控制物件的存取權。
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: 新物件的擁有者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975350"
---
# <a name="owner-of-a-new-object"></a><span data-ttu-id="8650b-104">新物件的擁有者</span><span class="sxs-lookup"><span data-stu-id="8650b-104">Owner of a New Object</span></span>

<span data-ttu-id="8650b-105">物件的擁有者隱含擁有 \_ 物件的寫入 DAC 存取權。</span><span class="sxs-lookup"><span data-stu-id="8650b-105">An object's owner implicitly has WRITE\_DAC access to the object.</span></span> <span data-ttu-id="8650b-106">這表示擁有者可以修改物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，因此可以控制物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="8650b-106">This means that the owner can modify the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), and thus, can control access to the object.</span></span>

<span data-ttu-id="8650b-107">新物件的擁有者是預設的擁有者 [*安全識別碼*](/windows/desktop/SecGloss/s-gly)， (SID) 來自建立 [*進程*](/windows/desktop/SecGloss/p-gly)的 [*主要*](/windows/desktop/SecGloss/p-gly)或模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。</span><span class="sxs-lookup"><span data-stu-id="8650b-107">The owner of a new object is the default owner [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creating [*process*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="8650b-108">若要取得或設定 [*存取權杖*](/windows/desktop/SecGloss/a-gly)中的預設擁有者，請使用 [**權杖 \_ 擁有**](/windows/desktop/api/Winnt/ns-winnt-token_owner)者結構來呼叫 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)或 [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)函數。</span><span class="sxs-lookup"><span data-stu-id="8650b-108">To get or set the default owner in an [*access token*](/windows/desktop/SecGloss/a-gly), call the [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-token_owner) structure.</span></span> <span data-ttu-id="8650b-109">系統不允許您將權杖的預設擁有者設定為不正確 SID，例如另一個使用者帳戶的 SID。</span><span class="sxs-lookup"><span data-stu-id="8650b-109">The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.</span></span>

<span data-ttu-id="8650b-110">啟用「SE \_ 取得擁有權」許可權的進程， \_ 可以將自己設定為物件的擁有者。</span><span class="sxs-lookup"><span data-stu-id="8650b-110">A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object.</span></span> <span data-ttu-id="8650b-111">啟用「SE \_ 還原名稱」 \_ 許可權或具有該物件之「寫入擁有者」存取權的進程， \_ 可以將任何有效的使用者或群組 SID 設定為物件的擁有者。</span><span class="sxs-lookup"><span data-stu-id="8650b-111">A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.</span></span>

 

 
