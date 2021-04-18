---
title: 安全性主體
description: 在 Windows 2000 中，安全性主體是使用者、群組或電腦 \ 8212;安全性系統可辨識的實體。
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- 安全性主體廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964953"
---
# <a name="security-principals"></a><span data-ttu-id="89c22-104">安全性主體</span><span class="sxs-lookup"><span data-stu-id="89c22-104">Security Principals</span></span>

<span data-ttu-id="89c22-105">在 Windows 2000 中，安全性主體是一個使用者、群組或電腦，也就是安全性系統可辨識的實體。</span><span class="sxs-lookup"><span data-stu-id="89c22-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="89c22-106">這包括人類使用者和自發流程。</span><span class="sxs-lookup"><span data-stu-id="89c22-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="89c22-107">嚴格來說，安全性系統無法分辨登入的使用者與電腦上執行的處理常式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="89c22-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="89c22-108">它會同時以安全性主體名稱的形式來查看安全性主體。</span><span class="sxs-lookup"><span data-stu-id="89c22-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="89c22-109">系統會建立使用者、群組和電腦，並將其儲存為 Active Directory Domain Services 中的物件。</span><span class="sxs-lookup"><span data-stu-id="89c22-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="89c22-110">此外，也有已知的安全性主體，代表由 Windows 2000 安全性系統所定義的特殊身分識別，例如 Everyone、Local System、Principal Self、已驗證的使用者、Creator Owner 等等。</span><span class="sxs-lookup"><span data-stu-id="89c22-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="89c22-111">代表知名安全性主體（例如匿名登入）的物件會儲存在設定容器底下的 W w n 安全性主體容器中。</span><span class="sxs-lookup"><span data-stu-id="89c22-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




