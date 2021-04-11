---
description: 如果此系統原則設定為1，安裝程式就不會在安裝期間儲存復原檔案，並停用安裝復原。
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943577"
---
# <a name="disablerollback"></a><span data-ttu-id="9e595-103">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="9e595-103">DisableRollback</span></span>

<span data-ttu-id="9e595-104">如果此 [系統原則](system-policy.md) 設定為1，安裝程式就不會在安裝期間儲存復原檔案，並停用安裝復原。</span><span class="sxs-lookup"><span data-stu-id="9e595-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="9e595-105">預設會啟用復原。</span><span class="sxs-lookup"><span data-stu-id="9e595-105">By default, rollback is enabled.</span></span> <span data-ttu-id="9e595-106">除非系統管理員絕對必要，否則建議不要使用此原則。</span><span class="sxs-lookup"><span data-stu-id="9e595-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="9e595-107">如需詳細資訊，請參閱 [復原安裝](rollback-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="9e595-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="9e595-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="9e595-108">Registry Key</span></span>

<span data-ttu-id="9e595-109">若要針對個別使用者安裝停用復原，請在下列登錄機碼底下將 **DisableRollback** 設定為1：</span><span class="sxs-lookup"><span data-stu-id="9e595-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="9e595-110">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="9e595-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="9e595-111">若要針對每部電腦安裝停用復原，請在下列登錄機碼底下將 **DisableRollback** 設定為1。</span><span class="sxs-lookup"><span data-stu-id="9e595-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="9e595-112">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="9e595-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="9e595-113">資料類型</span><span class="sxs-lookup"><span data-stu-id="9e595-113">Data Type</span></span>

<span data-ttu-id="9e595-114">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e595-114">**REG\_DWORD**</span></span>

 

 



