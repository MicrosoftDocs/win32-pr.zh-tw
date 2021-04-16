---
title: 網路管理功能安全性需求
description: 呼叫部分網路管理功能不需要特殊的群組成員資格。
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508080"
---
# <a name="network-management-function-security-requirements"></a><span data-ttu-id="06d3b-103">網路管理功能安全性需求</span><span class="sxs-lookup"><span data-stu-id="06d3b-103">Network management function security requirements</span></span>

<span data-ttu-id="06d3b-104">呼叫部分網路管理功能不需要特殊的群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="06d3b-104">Calling some of the network management functions does not require special group membership.</span></span> <span data-ttu-id="06d3b-105">其他函式要求使用者必須具備特定的許可權層級才能成功執行。</span><span class="sxs-lookup"><span data-stu-id="06d3b-105">Other functions require that users have a specific privilege level to execute successfully.</span></span> <span data-ttu-id="06d3b-106">當適用時，函式參考頁面上的 [備註] 區段會指出使用者執行特定函式時必須具備的許可權等級。</span><span class="sxs-lookup"><span data-stu-id="06d3b-106">When applicable, the Remarks section on a function's reference page indicates the privilege level a user must have to execute the particular function.</span></span>

<span data-ttu-id="06d3b-107">適用于 Active Directory 網域控制站的安全性需求可能與適用于伺服器和工作站的安全性需求不同。</span><span class="sxs-lookup"><span data-stu-id="06d3b-107">Security requirements that apply to Active Directory domain controllers can differ from those that apply to servers and workstations.</span></span>

<span data-ttu-id="06d3b-108">如需詳細資訊和受影響的函式清單，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="06d3b-108">For more information, and a list of affected functions, see the following topics:</span></span>

-   [<span data-ttu-id="06d3b-109">Active Directory 網域控制站上的網路管理功能需求</span><span class="sxs-lookup"><span data-stu-id="06d3b-109">Requirements for Network Management functions on Active Directory domain controllers</span></span>](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [<span data-ttu-id="06d3b-110">伺服器和工作站上網路管理功能的需求</span><span class="sxs-lookup"><span data-stu-id="06d3b-110">Requirements for Network Management functions on servers and workstations</span></span>](requirements-for-network-management-functions-on-servers-and-workstations.md)

<span data-ttu-id="06d3b-111">如需控制安全物件之存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)、 [許可權](/windows/desktop/SecAuthZ/privileges)和 [安全物件](/windows/desktop/SecAuthZ/securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="06d3b-111">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span>

<span data-ttu-id="06d3b-112">如需存取檢查期間所使用之特定安全描述項的詳細資訊，請參閱個別的函數參考頁面。</span><span class="sxs-lookup"><span data-stu-id="06d3b-112">For more information about specific security descriptors that are used during access checks, see the individual function reference page.</span></span> <span data-ttu-id="06d3b-113">如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="06d3b-113">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 