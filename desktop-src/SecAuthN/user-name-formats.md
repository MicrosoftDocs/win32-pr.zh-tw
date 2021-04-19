---
description: 當應用程式使用認證管理 API 提示輸入認證時，使用者應該輸入可由作業系統或應用程式驗證的資訊。
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: 使用者名稱格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980582"
---
# <a name="user-name-formats"></a><span data-ttu-id="ba418-103">使用者名稱格式</span><span class="sxs-lookup"><span data-stu-id="ba418-103">User Name Formats</span></span>

<span data-ttu-id="ba418-104">當應用程式使用認證管理 API 提示輸入認證時，使用者應該輸入可由作業系統或應用程式驗證的資訊。</span><span class="sxs-lookup"><span data-stu-id="ba418-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="ba418-105">使用者可以使用下列其中一種格式來指定網域認證資訊：</span><span class="sxs-lookup"><span data-stu-id="ba418-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="ba418-106">使用者主體名稱</span><span class="sxs-lookup"><span data-stu-id="ba418-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="ba418-107">下層登入名稱</span><span class="sxs-lookup"><span data-stu-id="ba418-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="ba418-108">使用者主體名稱</span><span class="sxs-lookup"><span data-stu-id="ba418-108">User Principal Name</span></span>

<span data-ttu-id="ba418-109">[*使用者主體名稱*](../secgloss/u-gly.md) (UPN) 格式是用來指定網際網路樣式的名稱，例如 <b>UserName@Example.Microsoft.com</b> 。</span><span class="sxs-lookup"><span data-stu-id="ba418-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="ba418-110">下表摘要說明 UPN 的各部分。</span><span class="sxs-lookup"><span data-stu-id="ba418-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="ba418-111">部分</span><span class="sxs-lookup"><span data-stu-id="ba418-111">Part</span></span>                                                        | <span data-ttu-id="ba418-112">範例</span><span class="sxs-lookup"><span data-stu-id="ba418-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ba418-113">使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-113">User account name.</span></span> <span data-ttu-id="ba418-114">也稱為登入名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="ba418-115">*使用者名稱*</span><span class="sxs-lookup"><span data-stu-id="ba418-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="ba418-116">分隔符號。</span><span class="sxs-lookup"><span data-stu-id="ba418-116">Separator.</span></span> <span data-ttu-id="ba418-117">字元常值，@ 符號 ( @ ) 。</span><span class="sxs-lookup"><span data-stu-id="ba418-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="ba418-118">UPN 尾碼。</span><span class="sxs-lookup"><span data-stu-id="ba418-118">UPN suffix.</span></span> <span data-ttu-id="ba418-119">也稱為功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="ba418-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="ba418-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="ba418-121">UPN 可以隱含或明確定義。</span><span class="sxs-lookup"><span data-stu-id="ba418-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="ba418-122">隱含 UPN 的格式為 <b>UserName@DNSDomainName.com</b> 。</span><span class="sxs-lookup"><span data-stu-id="ba418-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="ba418-123">即使未定義明確的 UPN，隱含的 UPN 一律會與使用者的帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="ba418-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="ba418-124">明確的 UPN 是表單 <i><b>Name@Suffix</b></i> ，系統管理員會明確定義名稱和尾碼字串。</span><span class="sxs-lookup"><span data-stu-id="ba418-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="ba418-125">Down-Level 登入名稱</span><span class="sxs-lookup"><span data-stu-id="ba418-125">Down-Level Logon Name</span></span>

<span data-ttu-id="ba418-126">下層登入名稱格式是用來指定網域和該網域中的使用者帳戶，例如 <i><b>網域 \\ </b></i>使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="ba418-127">下表摘要說明下層登入名稱的各部分。</span><span class="sxs-lookup"><span data-stu-id="ba418-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="ba418-128">部分</span><span class="sxs-lookup"><span data-stu-id="ba418-128">Part</span></span>                                                           | <span data-ttu-id="ba418-129">範例</span><span class="sxs-lookup"><span data-stu-id="ba418-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="ba418-130">NetBIOS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="ba418-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="ba418-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="ba418-132">分隔符號。</span><span class="sxs-lookup"><span data-stu-id="ba418-132">Separator.</span></span> <span data-ttu-id="ba418-133">字元常值， () 的反斜線 \\ 。</span><span class="sxs-lookup"><span data-stu-id="ba418-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="ba418-134">使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-134">User account name.</span></span> <span data-ttu-id="ba418-135">也稱為登入名稱。</span><span class="sxs-lookup"><span data-stu-id="ba418-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="ba418-136">*使用者名稱*</span><span class="sxs-lookup"><span data-stu-id="ba418-136">*UserName*</span></span><br/> |



 

 

 
