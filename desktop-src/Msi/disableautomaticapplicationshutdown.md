---
description: 如果每一電腦的系統原則設定為 1 (一) ，Windows Installer 不會與重新開機管理員互動，但它會使用 FilesInUse 對話方塊。如果每一電腦的系統原則設定為 2 (兩個) ，Windows Installer 會使用 FilesInUse 對話方塊。
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969314"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="92467-103">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="92467-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="92467-104">如果每一電腦的系統原則設定為 1 (一) ，Windows Installer 不會與 [重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal)互動，但是會使用 [FilesInUse 對話方塊](filesinuse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="92467-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="92467-105">如果每一電腦的系統原則設定為 2 (兩個) ，Windows Installer 會使用 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="92467-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="92467-106">這項設定會在安裝未撰寫為使用重新開機管理員的 Windows Installer 套件時，停用 [重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal) 可減輕重新開機的嘗試。</span><span class="sxs-lookup"><span data-stu-id="92467-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="92467-107">安裝程式仍會使用重新開機管理員來偵測應用程式所使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="92467-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="92467-108">從 Windows Vista Windows Installer 4.0 版開始提供 DisableAutomaticApplicationShutdown 原則。</span><span class="sxs-lookup"><span data-stu-id="92467-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="92467-109">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="92467-109">Registry Key</span></span>

<span data-ttu-id="92467-110">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="92467-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="92467-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="92467-111">Data Type</span></span>

<span data-ttu-id="92467-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="92467-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="92467-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="92467-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92467-114">**MSIRESTARTMANAGERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="92467-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="92467-115">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="92467-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
