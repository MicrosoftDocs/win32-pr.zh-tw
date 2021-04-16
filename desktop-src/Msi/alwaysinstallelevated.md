---
description: 使用提升的 (系統) 許可權安裝 Windows Installer 套件。
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513245"
---
# <a name="alwaysinstallelevated"></a><span data-ttu-id="f7813-103">AlwaysInstallElevated</span><span class="sxs-lookup"><span data-stu-id="f7813-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="f7813-104">您可以使用 AlwaysInstallElevated 原則，以提升的 (系統) 許可權來安裝 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="f7813-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="f7813-105">\* \* 警告： \* \*</span><span class="sxs-lookup"><span data-stu-id="f7813-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="f7813-106">此選項相當於授與完整的系統管理許可權，而這可能會造成大量的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="f7813-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="f7813-107">Microsoft 強烈不鼓勵使用此設定。</span><span class="sxs-lookup"><span data-stu-id="f7813-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="f7813-108">若要安裝具有提高許可權 (系統) 許可權的封裝，請在下列兩個登錄機碼底下將 AlwaysInstallElevated 值設為 "1"：</span><span class="sxs-lookup"><span data-stu-id="f7813-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="f7813-109">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f7813-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="f7813-110">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f7813-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="f7813-111">如果上述兩個登錄機碼底下的 AlwaysInstallElevated 值未設為 "1"，則安裝程式會使用較高的許可權來安裝受控應用程式，並針對未受管理的應用程式使用目前使用者的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="f7813-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="f7813-112">因為此原則允許使用者安裝需要存取使用者可能沒有許可權來存取目錄和登錄機碼的應用程式，所以您應該考慮它是否為您的使用者提供適當的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="f7813-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="f7813-113">設定此原則會指示 Windows Installer 在系統上安裝應用程式時使用系統許可權。</span><span class="sxs-lookup"><span data-stu-id="f7813-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="f7813-114">如果未設定此原則，系統會使用使用者的許可權來安裝未由系統管理員散發的應用程式，而且只有受管理的應用程式才會取得較高的許可權。</span><span class="sxs-lookup"><span data-stu-id="f7813-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="f7813-115">請注意，一旦啟用 AlwaysInstallElevated 的每一電腦原則，任何使用者都可以設定其每個使用者的設定。</span><span class="sxs-lookup"><span data-stu-id="f7813-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7813-116">備註</span><span class="sxs-lookup"><span data-stu-id="f7813-116">Remarks</span></span>

<span data-ttu-id="f7813-117">如需此原則與安裝來源互動的詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="f7813-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="f7813-118">資料類型</span><span class="sxs-lookup"><span data-stu-id="f7813-118">Data Type</span></span>

<span data-ttu-id="f7813-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f7813-119">**REG\_DWORD**</span></span>

 

 



