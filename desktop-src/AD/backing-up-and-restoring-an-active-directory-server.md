---
title: 備份與還原 Active Directory 伺服器
description: Active Directory Domain Services 提供在目錄資料庫中備份和還原資料的功能。
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services、使用、備份和還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681695"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="5a1d0-104">備份與還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="5a1d0-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="5a1d0-105">Active Directory Domain Services 提供在目錄資料庫中備份和還原資料的功能。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="5a1d0-106">本節說明如何 [備份](backing-up-an-active-directory-server.md) 和 [還原](restoring-an-active-directory-server.md) Active Directory 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="5a1d0-107">如需有關使用 Windows 2000 和 Windows Server 2003 作業系統中提供的公用程式來備份 Active Directory 伺服器的詳細資訊，請參閱 Microsoft TechNet 網站上的適用資源套件（英文）。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="5a1d0-108">Active Directory 伺服器的備份必須在線上執行，而且必須在安裝 Active Directory Domain Services 時執行。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="5a1d0-109">Active Directory Domain Services 是以特殊資料庫為基礎，並匯出一組提供程式設計備份介面的備份函式。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="5a1d0-110">備份不支援增量備份。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="5a1d0-111">備份應用程式會使用 Ntdsbcli 中定義的進入點，系結至本機用戶端 DLL。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="5a1d0-112">Active Directory 伺服器的還原一律會離線執行。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="5a1d0-113">雖然本節中的主題僅說明如何備份和還原 Active Directory 伺服器，但請注意，Windows 2000 和 Windows Server 2003 作業系統都有幾個必須同時備份和還原的「系統狀態」元件。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="5a1d0-114">這些系統狀態元件包含：</span><span class="sxs-lookup"><span data-stu-id="5a1d0-114">These system state components consist of:</span></span>

-   <span data-ttu-id="5a1d0-115">開機檔案，例如 ntldr、ntdetect、由 SFP 保護的所有檔案，以及效能計數器設定</span><span class="sxs-lookup"><span data-stu-id="5a1d0-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="5a1d0-116">Active Directory 網網域控制站</span><span class="sxs-lookup"><span data-stu-id="5a1d0-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="5a1d0-117">只有) 的 SysVol (網域控制站</span><span class="sxs-lookup"><span data-stu-id="5a1d0-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="5a1d0-118">只有) 的憑證伺服器 (CA</span><span class="sxs-lookup"><span data-stu-id="5a1d0-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="5a1d0-119">叢集資料庫 (叢集節點僅) </span><span class="sxs-lookup"><span data-stu-id="5a1d0-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="5a1d0-120">登錄</span><span class="sxs-lookup"><span data-stu-id="5a1d0-120">Registry</span></span>
-   <span data-ttu-id="5a1d0-121">COM + 類別註冊資料庫</span><span class="sxs-lookup"><span data-stu-id="5a1d0-121">COM+ class registration database</span></span>

<span data-ttu-id="5a1d0-122">系統狀態可以依任何順序進行備份，但是系統狀態的還原必須依照下列順序進行：</span><span class="sxs-lookup"><span data-stu-id="5a1d0-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="5a1d0-123">還原開機檔案。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="5a1d0-124">適當地還原 SysVol、憑證伺服器、叢集資料庫和 COM + 類別註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="5a1d0-125">還原 Active Directory 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="5a1d0-126">還原登錄。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-126">Restore the registry.</span></span>

<span data-ttu-id="5a1d0-127">如需有關備份和還原憑證服務的詳細資訊，請參閱 [使用憑證服務備份和還原功能](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions)。</span><span class="sxs-lookup"><span data-stu-id="5a1d0-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="5a1d0-128">如需備份和還原 Active Directory Domain Services 的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="5a1d0-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="5a1d0-129">Active Directory Domain Services 備份的考慮</span><span class="sxs-lookup"><span data-stu-id="5a1d0-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="5a1d0-130">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="5a1d0-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="5a1d0-131">還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="5a1d0-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="5a1d0-132">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="5a1d0-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 