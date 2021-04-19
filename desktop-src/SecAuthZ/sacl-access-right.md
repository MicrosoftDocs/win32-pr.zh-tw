---
description: 存取 \_ 系統 \_ 安全性存取權限可控制在物件安全描述項中取得或設定 SACL 的能力。 如果在 \_ \_ 要求的執行緒的存取權杖中啟用「SE 安全性名稱」許可權，系統就會授與此存取權。
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: SACL 存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973679"
---
# <a name="sacl-access-right"></a><span data-ttu-id="fb340-104">SACL 存取權限</span><span class="sxs-lookup"><span data-stu-id="fb340-104">SACL Access Right</span></span>

<span data-ttu-id="fb340-105">存取 \_ 系統 \_ 安全性存取權限可控制在物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中取得或設定 SACL 的能力。</span><span class="sxs-lookup"><span data-stu-id="fb340-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="fb340-106">只有在 \_ \_ 要求的執行緒的 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 中啟用「SE 安全性名稱」許可權時，系統才會授與此存取權限。</span><span class="sxs-lookup"><span data-stu-id="fb340-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="fb340-107">**存取物件的 SACL**</span><span class="sxs-lookup"><span data-stu-id="fb340-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="fb340-108">呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函式，以啟用「SE \_ 安全性名稱」 \_ 許可權。</span><span class="sxs-lookup"><span data-stu-id="fb340-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="fb340-109">\_ \_ 當您開啟物件的控制碼時，要求存取系統安全性存取權限。</span><span class="sxs-lookup"><span data-stu-id="fb340-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="fb340-110">使用 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 或 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)等函數來取得或設定物件的 SACL。</span><span class="sxs-lookup"><span data-stu-id="fb340-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="fb340-111">呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 以停用「SE \_ 安全性 \_ 名稱」許可權。</span><span class="sxs-lookup"><span data-stu-id="fb340-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="fb340-112">若要使用 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 或 [**SETNAMEDSECURITYINFO**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 函數存取 SACL，請啟用 [SE \_ 安全性 \_ 名稱] 許可權。</span><span class="sxs-lookup"><span data-stu-id="fb340-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="fb340-113">函數會在內部要求存取權限。</span><span class="sxs-lookup"><span data-stu-id="fb340-113">The function internally requests the access right.</span></span>

<span data-ttu-id="fb340-114">存取 \_ 系統 \_ 安全性存取權限在 dacl 中無效，因為 dacl 無法控制 SACL 的存取權。</span><span class="sxs-lookup"><span data-stu-id="fb340-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="fb340-115">不過，您可以使用 SACL 中的「存取 \_ 系統安全性」存取權限， \_ 來審查使用存取權限的嘗試。</span><span class="sxs-lookup"><span data-stu-id="fb340-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
