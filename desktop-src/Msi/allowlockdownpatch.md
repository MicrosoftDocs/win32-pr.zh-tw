---
description: 如果未設定每部電腦的系統原則，則只有系統管理員可以修補使用較高許可權安裝的現有產品。
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944036"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="f4d22-103">AllowLockdownPatch</span><span class="sxs-lookup"><span data-stu-id="f4d22-103">AllowLockdownPatch</span></span>

<span data-ttu-id="f4d22-104">如果未設定每部電腦的 [系統原則](system-policy.md) ，則只有系統管理員可以修補使用較高許可權安裝的現有產品。</span><span class="sxs-lookup"><span data-stu-id="f4d22-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="f4d22-105">如果 AllowLockdownPatch 設為 "1"，非系統管理員的使用者在某些情況下，可以在使用較高的許可權執行安裝時，將修補程式套用至產品。</span><span class="sxs-lookup"><span data-stu-id="f4d22-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="f4d22-106">使用原則設定之後，修補程式就可以在使用較高的許可權執行安裝時安裝 [次要升級](minor-upgrades.md) ，修補程式無法安裝 [主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="f4d22-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="f4d22-107">設定此原則也可讓非系統管理員的使用者在提高許可權的安裝期間，以 LocalSystem 許可權執行程式。</span><span class="sxs-lookup"><span data-stu-id="f4d22-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="f4d22-108">建議使用預設設定，以確保安全的環境。</span><span class="sxs-lookup"><span data-stu-id="f4d22-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="f4d22-109">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="f4d22-109">Registry Key</span></span>

<span data-ttu-id="f4d22-110">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f4d22-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f4d22-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="f4d22-111">Data Type</span></span>

<span data-ttu-id="f4d22-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f4d22-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f4d22-113">備註</span><span class="sxs-lookup"><span data-stu-id="f4d22-113">Remarks</span></span>

<span data-ttu-id="f4d22-114">任何使用者都可以在 nonelevated 安裝期間套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="f4d22-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="f4d22-115">將此每部電腦的 [系統原則](system-policy.md) 設定為 "1"，可讓非系統管理員的使用者在提高許可權的安裝期間，將修補程式套用至任何產品的額外彈性。</span><span class="sxs-lookup"><span data-stu-id="f4d22-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="f4d22-116">如果未設定此原則，非管理員使用者就無法將修補程式套用至已指派或已發佈的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f4d22-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="f4d22-117">如果有安裝或啟動這些程式的 Windows Installer patch 套件，則設定此原則也可讓非系統管理員的使用者以 LocalSystem 許可權執行任意程式。</span><span class="sxs-lookup"><span data-stu-id="f4d22-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



