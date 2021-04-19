---
description: 支援在 c + + 中使用授權所列出的主要工作。
ms.assetid: f3300cfb-39e4-4ce8-8310-1531208bcd34
title: 在 c + + 中支援授權的工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3dab3535b8f80b0118f9c020148aaab83f3361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974944"
---
# <a name="supporting-tasks-for-authorization-in-c"></a><span data-ttu-id="6601b-103">在 c + + 中支援授權的工作</span><span class="sxs-lookup"><span data-stu-id="6601b-103">Supporting Tasks for Authorization in C++</span></span>

<span data-ttu-id="6601b-104">下列工作支援在 [c + + 中使用授權](using-authorization-in-c--.md)所列出的主要工作。</span><span class="sxs-lookup"><span data-stu-id="6601b-104">The following tasks support the main tasks listed in [Using Authorization in C++](using-authorization-in-c--.md).</span></span>



| <span data-ttu-id="6601b-105">主題</span><span class="sxs-lookup"><span data-stu-id="6601b-105">Topic</span></span>                                                                                                                                  | <span data-ttu-id="6601b-106">描述</span><span class="sxs-lookup"><span data-stu-id="6601b-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6601b-107">在 c + + 中建立授權原則存放區</span><span class="sxs-lookup"><span data-stu-id="6601b-107">Creating an Authorization Policy Store in C++</span></span>](creating-an-authorization-policy-store-in-c--.md)                                     | <span data-ttu-id="6601b-108">在安裝應用程式之前或期間建立授權原則。</span><span class="sxs-lookup"><span data-stu-id="6601b-108">Create an authorization policy before or during the installation of an application.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="6601b-109">使用 c + + 中的授權管理員建立用戶端內容</span><span class="sxs-lookup"><span data-stu-id="6601b-109">Establishing a Client Context with Authorization Manager in C++</span></span>](establishing-a-client-context-with-authorization-manager-in-c--.md) | <span data-ttu-id="6601b-110">使用權杖的控制碼、網域和使用者名稱，或用戶端的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 的字串表示，建立用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="6601b-110">Create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span> |
| [<span data-ttu-id="6601b-111">在 c + + 中使用商務邏輯來限定存取權</span><span class="sxs-lookup"><span data-stu-id="6601b-111">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)                                       | <span data-ttu-id="6601b-112">提供用來檢查存取的執行時間邏輯。</span><span class="sxs-lookup"><span data-stu-id="6601b-112">Provide run-time logic for checking access.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="6601b-113">在 c + + 中使用 Acl 定義許可權</span><span class="sxs-lookup"><span data-stu-id="6601b-113">Defining Permissions with ACLs in C++</span></span>](defining-permissions-with-acls-in-c--.md)                                                     | <span data-ttu-id="6601b-114">藉由建立及修改與這些資源相關聯的 Acl，以及啟用和停用用戶端許可權，來定義哪些用戶端可以存取哪些資源。</span><span class="sxs-lookup"><span data-stu-id="6601b-114">Define which clients have access to which resources by creating and modifying the ACLs associated with those resources and by enabling and disabling client privileges.</span></span>                                                                      |
| [<span data-ttu-id="6601b-115">從 c + + 中的 SID 建立用戶端內容</span><span class="sxs-lookup"><span data-stu-id="6601b-115">Establishing a Client Context from a SID in C++</span></span>](establishing-a-client-context-from-a-sid-in-c--.md)                                 | <span data-ttu-id="6601b-116">識別使用者、群組或電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6601b-116">Identify a user, group, or computer account.</span></span> <span data-ttu-id="6601b-117">使用 Sid 來檢查資源的存取權限。</span><span class="sxs-lookup"><span data-stu-id="6601b-117">Use SIDs to check access rights to resources.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="6601b-118">在 c + + 中使用 Acl 確認用戶端存取</span><span class="sxs-lookup"><span data-stu-id="6601b-118">Verifying Client Access with ACLs in C++</span></span>](verifying-client-access-with-acls-in-c--.md)                                               | <span data-ttu-id="6601b-119">檢查 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 允許用戶端的存取權限。</span><span class="sxs-lookup"><span data-stu-id="6601b-119">Check the access rights that a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows for a client.</span></span>                                                                              |
| [<span data-ttu-id="6601b-120">在 c + + 中尋找檔案物件的擁有者</span><span class="sxs-lookup"><span data-stu-id="6601b-120">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)                                             | <span data-ttu-id="6601b-121">尋找並列印檔案擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6601b-121">Find and print the name of the owner of a file.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="6601b-122">以 c + + 取得物件擁有權</span><span class="sxs-lookup"><span data-stu-id="6601b-122">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)                                                                   | <span data-ttu-id="6601b-123">藉由取得該物件的擁有權來變更檔案物件的 DACL。</span><span class="sxs-lookup"><span data-stu-id="6601b-123">Change the DACL of a file object by taking ownership of that object.</span></span>                                                                                                                                                                         |



 

 

 
