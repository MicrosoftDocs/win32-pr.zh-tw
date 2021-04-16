---
description: 如果 Windows Installer 套件安裝或通告元件，安裝程式會將這些元件的相關資訊儲存在本機系統登錄中。
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Windows Installer 所寫入的元件登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513240"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="b9f2f-103">Windows Installer 所寫入的元件登錄機碼</span><span class="sxs-lookup"><span data-stu-id="b9f2f-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="b9f2f-104">如果 Windows Installer 套件安裝或通告元件，安裝程式會將這些元件的相關資訊儲存在本機系統登錄中。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="b9f2f-105">請注意，這些登錄機碼僅供 Windows Installer 在內部使用，且不應由您的應用程式來依賴。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="b9f2f-106">這些機碼中儲存的資訊內容、位置和結構可能會變更。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="b9f2f-107">應用程式應該依賴 [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) 管理元件。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="b9f2f-108">元件是由元件名稱所註冊。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="b9f2f-109">儲存在下列位置的值名稱是元件名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="b9f2f-110">實際值的類型為 REG \_ 多重 \_ SZ，並且包含 [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) 用來安裝或修復元件的資料。</span><span class="sxs-lookup"><span data-stu-id="b9f2f-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="b9f2f-111">私用元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b9f2f-111">Information About Private Assemblies</span></span>

<span data-ttu-id="b9f2f-112">Windows Installer 會儲存在下列登錄機碼下已安裝為受管理的每個使用者應用程式之私用元件 Windows Installer 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="b9f2f-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="b9f2f-113">**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**安裝程式** \\**受控** \\**_使用者 SID_ *_\\_*** \\  \\ \* *_設定檔的_* 安裝程式元件路徑 _</span><span class="sxs-lookup"><span data-stu-id="b9f2f-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="b9f2f-114">Windows Installer 會儲存在下列登錄機碼下依使用者安裝的 Windows Installer 套件所攜帶之私用元件的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="b9f2f-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="b9f2f-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** 元件 **\\** _至設定檔的路徑_*_</span><span class="sxs-lookup"><span data-stu-id="b9f2f-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="b9f2f-116">Windows Installer 儲存 Windows Installer 套件所攜帶之私用元件的相關資訊，並在下列登錄機碼下依電腦安裝：</span><span class="sxs-lookup"><span data-stu-id="b9f2f-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="b9f2f-117">_*HKLM **\\** 軟體 **\\** 類別 **\\** 安裝 **\\** 程式元件 **\\** _至設定檔的路徑_*_</span><span class="sxs-lookup"><span data-stu-id="b9f2f-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="b9f2f-118">全域或共用元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b9f2f-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="b9f2f-119">Windows Installer 會儲存在下列登錄機碼下已安裝為受管理之每個使用者應用程式的 Windows Installer 套件所攜帶的共用元件的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="b9f2f-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="b9f2f-120">_*HKLM **\\** 軟體 **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** 管理的 **\\** _使用者 SID_*_ \\ _ *安裝 **\\** 程式元件 **\\** 全域*\*</span><span class="sxs-lookup"><span data-stu-id="b9f2f-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="b9f2f-121">Windows Installer 會儲存在下列登錄機碼下，針對每位使用者安裝的 Windows Installer 套件所攜帶的共用元件的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="b9f2f-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="b9f2f-122">**HKCU** \\**軟體** \\**Microsoft** \\**安裝程式** \\**元件** \\**全域**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="b9f2f-123">Windows Installer 儲存 Windows Installer 封裝所攜帶的共用元件的相關資訊，並在下列登錄機碼下依電腦安裝：</span><span class="sxs-lookup"><span data-stu-id="b9f2f-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="b9f2f-124">**HKLM** \\**軟體** \\**類別** \\**安裝程式** \\**元件** \\**全域**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



