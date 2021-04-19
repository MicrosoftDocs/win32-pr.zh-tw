---
description: 當 (SSP) 安全性套件建立安全性支援提供者時，您不應該允許加入網域的用戶端使用下列格式的兩個元件服務提供者名稱 (SPN) 來驗證網域控制站。
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: 使用三部分主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970154"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="e9855-103">使用三部分主體名稱</span><span class="sxs-lookup"><span data-stu-id="e9855-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="e9855-104">當 (SSP) 安全性套件建立安全性支援提供者時，您不應該允許加入網域的用戶端使用下列格式的兩個元件服務提供者名稱 (SPN) 來驗證網域控制站。</span><span class="sxs-lookup"><span data-stu-id="e9855-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="e9855-105"><*通訊協定* >/<*主機名稱*></span><span class="sxs-lookup"><span data-stu-id="e9855-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="e9855-106">用戶端應該一律藉由指定網域來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e9855-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="e9855-107"><*通訊協定* >/<*主機名稱* >/<*功能變數名稱*></span><span class="sxs-lookup"><span data-stu-id="e9855-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="e9855-108">加入網域的用戶端若以兩部分 SPN 登入，可能就可以模擬網域控制站。</span><span class="sxs-lookup"><span data-stu-id="e9855-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="e9855-109">如果您允許兩部分 Spn，您應該建立包含足夠資訊的記錄專案，讓系統管理員能夠識別呼叫者。</span><span class="sxs-lookup"><span data-stu-id="e9855-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



