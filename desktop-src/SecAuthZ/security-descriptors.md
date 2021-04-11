---
description: 安全描述項包含與安全物件相關聯的安全性資訊。
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: 安全性描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848235"
---
# <a name="security-descriptors"></a><span data-ttu-id="b493b-103">安全性描述項</span><span class="sxs-lookup"><span data-stu-id="b493b-103">Security Descriptors</span></span>

<span data-ttu-id="b493b-104">[*安全描述項*](/windows/desktop/SecGloss/s-gly)包含與安全 [物件](securable-objects.md)相關聯的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="b493b-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="b493b-105">安全描述項是由 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) 結構與其相關聯的安全性資訊所組成。</span><span class="sxs-lookup"><span data-stu-id="b493b-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="b493b-106">安全描述項可包含下列安全性資訊：</span><span class="sxs-lookup"><span data-stu-id="b493b-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="b493b-107">物件的擁有者和主要群組 (Sid) 的[安全識別碼](security-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="b493b-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="b493b-108">[DACL](access-control-lists.md) ，指定允許或拒絕特定使用者或群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="b493b-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="b493b-109">[SACL](access-control-lists.md) ，指定產生物件之審核記錄的存取嘗試類型。</span><span class="sxs-lookup"><span data-stu-id="b493b-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="b493b-110">限定安全描述項或其個別成員意義的一組控制位。</span><span class="sxs-lookup"><span data-stu-id="b493b-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="b493b-111">應用程式不能直接操作安全描述項的內容。</span><span class="sxs-lookup"><span data-stu-id="b493b-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="b493b-112">Windows API 提供的函式可設定和取得物件安全描述項中的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="b493b-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="b493b-113">此外，還有一些函數可用於建立及初始化新物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b493b-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="b493b-114">使用 Active Directory 物件上安全描述項的應用程式可以使用 Windows 安全性函式或 Active Directory 服務介面所提供的安全性介面 (ADSI) 。</span><span class="sxs-lookup"><span data-stu-id="b493b-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="b493b-115">如需 ADSI 安全性介面的詳細資訊，請參閱 [Active Directory 中的存取控制的運作方式](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services)。</span><span class="sxs-lookup"><span data-stu-id="b493b-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 
