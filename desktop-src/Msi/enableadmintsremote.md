---
description: 從 Windows Server 2008 和 Windows Vista 開始，此原則不再具有任何作用。
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191872"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="921e9-103">EnableAdminTSRemote</span><span class="sxs-lookup"><span data-stu-id="921e9-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="921e9-104">從 Windows Server 2008 和 Windows Vista 開始，此原則不再具有任何作用。</span><span class="sxs-lookup"><span data-stu-id="921e9-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="921e9-105">系統管理員可以從終端機伺服器的主控台會話執行安裝。</span><span class="sxs-lookup"><span data-stu-id="921e9-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="921e9-106">系統管理員也可以從終端機伺服器的用戶端會話執行安裝。</span><span class="sxs-lookup"><span data-stu-id="921e9-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="921e9-107">如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的 [終端機服務](/windows/desktop/TermServ/terminal-services-portal) 。</span><span class="sxs-lookup"><span data-stu-id="921e9-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="921e9-108">\* \* 早于 Windows Server 2008 和 Windows Vista 的作業系統： \* \*</span><span class="sxs-lookup"><span data-stu-id="921e9-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="921e9-109">設定每一電腦的 [系統原則](system-policy.md) ，可讓系統管理員從終端機伺服器的用戶端會話執行安裝。</span><span class="sxs-lookup"><span data-stu-id="921e9-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="921e9-110">如果未設定此原則，系統管理員只能從主控台會話執行安裝。</span><span class="sxs-lookup"><span data-stu-id="921e9-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="921e9-111">非管理員的使用者永遠不能從用戶端會話執行安裝。</span><span class="sxs-lookup"><span data-stu-id="921e9-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="921e9-112">此原則的預設值僅允許系統管理員從主控台會話執行安裝。</span><span class="sxs-lookup"><span data-stu-id="921e9-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="921e9-113">系統管理員一律可以從終端機伺服器的用戶端會話，或從主控台會話進行系統 [管理安裝](administrative-installation.md) ，不論是否已設定此原則。</span><span class="sxs-lookup"><span data-stu-id="921e9-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="921e9-114">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="921e9-114">Registry Key</span></span>

<span data-ttu-id="921e9-115">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="921e9-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="921e9-116">資料類型</span><span class="sxs-lookup"><span data-stu-id="921e9-116">Data Type</span></span>

<span data-ttu-id="921e9-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="921e9-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="921e9-118">備註</span><span class="sxs-lookup"><span data-stu-id="921e9-118">Remarks</span></span>

<span data-ttu-id="921e9-119">如需詳細資訊，請參閱搭配 [使用 Windows Installer 與終端機伺服器](using-windows-installer-with-a-terminal-server.md)。</span><span class="sxs-lookup"><span data-stu-id="921e9-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 
