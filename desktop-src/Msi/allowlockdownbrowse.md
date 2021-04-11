---
description: 將此每部電腦系統原則的值設定為 &\# 0034; 1&\# 0034; 可讓非系統管理員的使用者使用 [流覽] 對話方塊來找出受管理應用程式的來源。
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848981"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="087af-103">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="087af-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="087af-104">將每部電腦 [系統原則](system-policy.md) 的值設定為 "1"，可讓非系統管理員的使用者使用 [[流覽] 對話方塊](browse-dialog.md) 來找出 [*受管理應用程式*](m-gly.md)的來源。</span><span class="sxs-lookup"><span data-stu-id="087af-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="087af-105">來源可能包含媒體，例如 CD-ROM、Url 和網路位置。</span><span class="sxs-lookup"><span data-stu-id="087af-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="087af-106">如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="087af-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="087af-107">Windows Installer 的預設值是，非受控使用者無法流覽受管理應用程式的新來源。</span><span class="sxs-lookup"><span data-stu-id="087af-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="087af-108">唯一可用的來源是已在產品的來源清單中註冊的來源。</span><span class="sxs-lookup"><span data-stu-id="087af-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="087af-109">如果設定此原則，非系統管理員的使用者可能會流覽已指派或已發佈應用程式的新來源，或針對所有使用者安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="087af-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="087af-110">設定 AllowLockdownBrowse 也可讓非系統管理員的使用者在提高許可權的安裝期間，以 LocalSystem 許可權執行程式。</span><span class="sxs-lookup"><span data-stu-id="087af-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="087af-111">建議使用預設設定，以確保安全的環境。</span><span class="sxs-lookup"><span data-stu-id="087af-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="087af-112">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="087af-112">Registry Key</span></span>

<span data-ttu-id="087af-113">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="087af-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="087af-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="087af-114">Data Type</span></span>

<span data-ttu-id="087af-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="087af-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="087af-116">備註</span><span class="sxs-lookup"><span data-stu-id="087af-116">Remarks</span></span>

<span data-ttu-id="087af-117">如果有安裝或啟動這些程式的 Windows Installer 套件，則設定此原則也可讓非系統管理員的使用者以 LocalSystem 許可權執行任意程式。</span><span class="sxs-lookup"><span data-stu-id="087af-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="087af-118">[DisableBrowse](disablebrowse.md) 會覆寫 AllowLockdownBrowse 並防止流覽，即使已設定 AllowLockdownBrowse 也是如此。</span><span class="sxs-lookup"><span data-stu-id="087af-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="087af-119">如需此原則與安裝來源互動的詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="087af-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="087af-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="087af-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087af-121">來源復原</span><span class="sxs-lookup"><span data-stu-id="087af-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="087af-122">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="087af-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



