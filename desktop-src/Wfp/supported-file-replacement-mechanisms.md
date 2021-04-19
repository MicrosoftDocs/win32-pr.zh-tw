---
description: 您可以透過下列機制來取代受保護的資源。
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: 支援的資源取代機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994478"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="20d51-103">支援的資源取代機制</span><span class="sxs-lookup"><span data-stu-id="20d51-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="20d51-104">您可以透過下列機制來取代受保護的資源。</span><span class="sxs-lookup"><span data-stu-id="20d51-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="20d51-105">在 Windows Vista 和 Windows Server 2008 上修改受 WRP 保護之資源的完整存取權，僅限於使用下列機制搭配 Windows 模組安裝程式服務 TrustedInstaller：</span><span class="sxs-lookup"><span data-stu-id="20d51-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="20d51-106">TrustedInstaller 安裝的 Windows Service Pack。</span><span class="sxs-lookup"><span data-stu-id="20d51-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="20d51-107">TrustedInstaller 安裝的修補程式。</span><span class="sxs-lookup"><span data-stu-id="20d51-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="20d51-108">TrustedInstaller 安裝的作業系統升級。</span><span class="sxs-lookup"><span data-stu-id="20d51-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="20d51-109">由 TrustedInstaller 安裝 Windows Update。</span><span class="sxs-lookup"><span data-stu-id="20d51-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="20d51-110">如果應用程式和安裝程式嘗試以 WRP 保護的資源取代這些指定方法以外的資源，則會拒絕變更資源並產生拒絕存取錯誤訊息的存取權。</span><span class="sxs-lookup"><span data-stu-id="20d51-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="20d51-111">對於嘗試取代受 WRP 保護之資源的知名安裝程式，可能會隱藏拒絕存取錯誤和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="20d51-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="20d51-112">在此情況下，作業會成功傳回，錯誤和錯誤訊息會隱藏，但不會對受 WRP 保護的資源套用任何變更。</span><span class="sxs-lookup"><span data-stu-id="20d51-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="20d51-113">只有在符合下列所有條件時，才可以針對已知的安裝程式隱藏此錯誤：</span><span class="sxs-lookup"><span data-stu-id="20d51-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="20d51-114">這是繼承應用程式。</span><span class="sxs-lookup"><span data-stu-id="20d51-114">This is a legacy application.</span></span> <span data-ttu-id="20d51-115">應用程式不包含並無 requestedexecutionlevel 的資訊清單，該資訊清單會識別針對 Windows Vista 或 Windows Server 2008 所設計的應用程式。</span><span class="sxs-lookup"><span data-stu-id="20d51-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="20d51-116">拒絕存取的錯誤是因為嘗試修改受 WRP 保護的資源所造成。</span><span class="sxs-lookup"><span data-stu-id="20d51-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="20d51-117">系統管理員正在安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="20d51-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="20d51-118">如需搭配 WRP 使用 Windows Installer 的詳細資訊，請參閱在[Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK 中[使用 Windows Installer 和 Windows 資源保護](/windows/desktop/Msi/windows-resource-protection-on-windows-vista)。</span><span class="sxs-lookup"><span data-stu-id="20d51-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="20d51-119">**Windows Server 2003 和 WINDOWS XP：** 只有透過下列機制，才支援更換受 WFP 保護的系統檔案：</span><span class="sxs-lookup"><span data-stu-id="20d51-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="20d51-120">使用 Update.exe 的 Windows Service Pack 安裝</span><span class="sxs-lookup"><span data-stu-id="20d51-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="20d51-121">使用 Hotfix.exe 安裝的修補程式</span><span class="sxs-lookup"><span data-stu-id="20d51-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="20d51-122">使用 Winnt32.exe 的作業系統升級</span><span class="sxs-lookup"><span data-stu-id="20d51-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="20d51-123">Windows Update</span><span class="sxs-lookup"><span data-stu-id="20d51-123">Windows Update</span></span>

<span data-ttu-id="20d51-124">以這些指定的方法取代受保護的檔案，會導致 WFP 還原原始檔案。</span><span class="sxs-lookup"><span data-stu-id="20d51-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 
