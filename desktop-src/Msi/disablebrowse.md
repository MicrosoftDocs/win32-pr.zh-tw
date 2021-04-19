---
description: 將每部電腦系統原則的值設定為 &\# 0034; 1&\# 0034; 防止非系統管理員的使用者使用 [流覽] 對話方塊來找出儲存在媒體上的受管理應用程式來源，例如 cd-rom。
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991688"
---
# <a name="disablebrowse"></a><span data-ttu-id="beb9a-103">DisableBrowse</span><span class="sxs-lookup"><span data-stu-id="beb9a-103">DisableBrowse</span></span>

<span data-ttu-id="beb9a-104">將此每部電腦 [系統原則](system-policy.md) 的值設定為 "1"，可防止非系統管理員的使用者使用 [[流覽] 對話方塊](browse-dialog.md) 來找出儲存在媒體上的 [*受管理應用程式*](m-gly.md) 來源，例如 cd-rom。</span><span class="sxs-lookup"><span data-stu-id="beb9a-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="beb9a-105">直接輸入的 [使用功能來源：] 下拉式方塊已鎖定，而 [流覽 ...]按鈕已停用。</span><span class="sxs-lookup"><span data-stu-id="beb9a-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="beb9a-106">如需有關來源流覽的詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="beb9a-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="beb9a-107">DisableBrowse 會覆寫 AllowLockdownBrowse 並防止流覽，即使已設定 AllowLockdownBrowse 也是如此。</span><span class="sxs-lookup"><span data-stu-id="beb9a-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="beb9a-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="beb9a-108">Registry Key</span></span>

<span data-ttu-id="beb9a-109">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="beb9a-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="beb9a-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="beb9a-110">Data Type</span></span>

<span data-ttu-id="beb9a-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="beb9a-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="beb9a-112">備註</span><span class="sxs-lookup"><span data-stu-id="beb9a-112">Remarks</span></span>

<span data-ttu-id="beb9a-113">在 DisableBrowse 設定的某些情況下，非管理使用者可能仍然能夠從正確標示的媒體上的來源安裝受控應用程式。</span><span class="sxs-lookup"><span data-stu-id="beb9a-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="beb9a-114">設定 DisableBrowse 原則只會停用流覽至來源的功能。</span><span class="sxs-lookup"><span data-stu-id="beb9a-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="beb9a-115">您可以使用它來防止非系統管理員的使用者在安裝隨選安裝、重新安裝或修復期間流覽至新的來源。</span><span class="sxs-lookup"><span data-stu-id="beb9a-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="beb9a-116">如果設定了 [AllowLockdownMedia](allowlockdownmedia.md) ，則非管理的使用者仍然可以從正確標示的媒體安裝受控應用程式。</span><span class="sxs-lookup"><span data-stu-id="beb9a-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="beb9a-117">DisableBrowse 可防止非管理員使用者流覽至新的媒體位置或任何其他來源位置。</span><span class="sxs-lookup"><span data-stu-id="beb9a-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="beb9a-118">如需如何保護受控應用程式之媒體來源的詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="beb9a-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="beb9a-119">如需此原則與安裝來源互動的詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="beb9a-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



