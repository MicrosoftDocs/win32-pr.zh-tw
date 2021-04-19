---
description: 您可以使用本機安全性原則 Microsoft Management Console (MMC) 嵌入式管理單元 () Secpol.msc 或呼叫 LsaAddAccountRights 函式，將許可權指派給帳戶。
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: 將許可權指派給帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980567"
---
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="ab6f7-103">將許可權指派給帳戶</span><span class="sxs-lookup"><span data-stu-id="ab6f7-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="ab6f7-104">您可以使用本機安全性原則 Microsoft Management Console (MMC) 嵌入式管理單元 () Secpol.msc 或呼叫 [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) 函式，將許可權指派給帳戶。</span><span class="sxs-lookup"><span data-stu-id="ab6f7-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="ab6f7-105">將許可權指派給帳戶並不會影響現有的使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="ab6f7-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="ab6f7-106">使用者必須登出再重新登入，才能取得具有新指派許可權的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="ab6f7-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="ab6f7-107">若要使用 [本機安全性原則] MMC 嵌入式管理單元指派許可權，請編輯 [ **安全性設定/本機原則/使用者權限指派**] 底下列出的每個許可權的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="ab6f7-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
