---
description: 某些函數需要特殊許可權才能正確執行。
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: 以特殊許可權執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983888"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="5d43d-103">以特殊許可權執行</span><span class="sxs-lookup"><span data-stu-id="5d43d-103">Running with Special Privileges</span></span>

<span data-ttu-id="5d43d-104">某些函數需要特殊 [許可權](/windows/desktop/SecAuthZ/privileges) 才能正確執行。</span><span class="sxs-lookup"><span data-stu-id="5d43d-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="5d43d-105">在某些情況下，函數只能由特定使用者或特定群組的成員執行。</span><span class="sxs-lookup"><span data-stu-id="5d43d-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="5d43d-106">最常見的需求是使用者是本機系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5d43d-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="5d43d-107">其他函式要求使用者的帳戶必須啟用特定許可權。</span><span class="sxs-lookup"><span data-stu-id="5d43d-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="5d43d-108">為了降低未經授權的程式碼能夠取得控制權的可能性，系統應該以所需的最低許可權來執行。</span><span class="sxs-lookup"><span data-stu-id="5d43d-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="5d43d-109">需要呼叫需要特殊許可權之函式的應用程式，可能會讓系統保持在駭客攻擊的狀態。</span><span class="sxs-lookup"><span data-stu-id="5d43d-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="5d43d-110">這類應用程式應該設計成在短時間內執行，而且應該告知使用者相關的安全性含意。</span><span class="sxs-lookup"><span data-stu-id="5d43d-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="5d43d-111">如需如何以不同的使用者執行，以及如何在您的應用程式中啟用許可權的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="5d43d-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="5d43d-112">以系統管理員許可權執行</span><span class="sxs-lookup"><span data-stu-id="5d43d-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="5d43d-113">要求使用者提供認證</span><span class="sxs-lookup"><span data-stu-id="5d43d-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="5d43d-114">變更權杖中的許可權</span><span class="sxs-lookup"><span data-stu-id="5d43d-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="5d43d-115">將許可權指派給帳戶</span><span class="sxs-lookup"><span data-stu-id="5d43d-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
