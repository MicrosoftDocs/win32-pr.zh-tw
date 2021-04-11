---
description: 這是每一電腦的系統原則，可在系統管理員只想要安裝每一部電腦的應用程式時使用。
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112276"
---
# <a name="disableuserinstalls"></a><span data-ttu-id="fcef9-103">DisableUserInstalls</span><span class="sxs-lookup"><span data-stu-id="fcef9-103">DisableUserInstalls</span></span>

<span data-ttu-id="fcef9-104">這是每一電腦的 [系統原則](system-policy.md) ，可在系統管理員只想要安裝每一部電腦的應用程式時使用。</span><span class="sxs-lookup"><span data-stu-id="fcef9-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="fcef9-105">如果未設定此原則，安裝程式會依下列順序搜尋應用程式的登錄：管理的應用程式會註冊為每位使用者、每位使用者註冊的非受控應用程式，最後是註冊為每部電腦的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fcef9-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="fcef9-106">如果此原則設定為1，則安裝程式會忽略所有註冊為每個使用者的應用程式，而且只會搜尋以每部電腦方式註冊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fcef9-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="fcef9-107">Windows Installer 應用程式開發介面或系統的呼叫會忽略每個使用者的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fcef9-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="fcef9-108">嘗試在每個使用者 [安裝內容](installation-context.md) 中執行安裝，會導致安裝程式顯示錯誤訊息並停止安裝。</span><span class="sxs-lookup"><span data-stu-id="fcef9-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="fcef9-109">在此情況下，Windows Installer 也會防止終端機伺服器的每個使用者安裝。</span><span class="sxs-lookup"><span data-stu-id="fcef9-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fcef9-110">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="fcef9-110">Registry Key</span></span>

<span data-ttu-id="fcef9-111">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="fcef9-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="fcef9-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="fcef9-112">Data Type</span></span>

<span data-ttu-id="fcef9-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fcef9-113">**REG\_DWORD**</span></span>

 

 



