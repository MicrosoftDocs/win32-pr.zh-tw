---
description: 如果每一電腦的系統原則設定為1，則不能由使用者或系統管理員從電腦移除修補程式。
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848253"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="cd3e6-103">DisablePatchUninstall</span><span class="sxs-lookup"><span data-stu-id="cd3e6-103">DisablePatchUninstall</span></span>

<span data-ttu-id="cd3e6-104">如果每一電腦的 [系統原則](system-policy.md) 設定為1，則不能由使用者或系統管理員從電腦移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="cd3e6-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="cd3e6-105">Windows Installer 仍然可以移除不再適用于產品的修補程式。</span><span class="sxs-lookup"><span data-stu-id="cd3e6-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="cd3e6-106">如果未設定此原則，只有當使用者已獲得移除修補程式的許可權時，使用者才可以從電腦移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="cd3e6-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="cd3e6-107">這取決於使用者是否為系統管理員、是否已設定 [DisableMsi](disablemsi.md) 和 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則設定，以及修補程式是否安裝在每個使用者管理、每個使用者的非受控或個別電腦內容中。</span><span class="sxs-lookup"><span data-stu-id="cd3e6-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="cd3e6-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="cd3e6-108">Registry Key</span></span>

<span data-ttu-id="cd3e6-109">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="cd3e6-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="cd3e6-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="cd3e6-110">Data Type</span></span>

<span data-ttu-id="cd3e6-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd3e6-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd3e6-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd3e6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd3e6-113">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="cd3e6-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



