---
description: 將 TransformsSecure 原則設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: TransformsSecure 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847683"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="489d9-103">TransformsSecure 原則</span><span class="sxs-lookup"><span data-stu-id="489d9-103">TransformsSecure Policy</span></span>

<span data-ttu-id="489d9-104">將 TransformsSecure 原則設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。</span><span class="sxs-lookup"><span data-stu-id="489d9-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="489d9-105">設定此原則與設定 [TRANSFORMSSECURE 屬性](transformssecure.md) 相同，不同之處在于範圍不同。</span><span class="sxs-lookup"><span data-stu-id="489d9-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="489d9-106">設定 TransformsSecure 原則會套用至安裝至指定電腦的所有套件。</span><span class="sxs-lookup"><span data-stu-id="489d9-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="489d9-107">無論電腦為何，設定 TRANSFORMSSECURE 屬性都會套用至封裝。</span><span class="sxs-lookup"><span data-stu-id="489d9-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="489d9-108">此原則的目的是要為安全轉換儲存提供 Windows 2000 的旅遊使用者。</span><span class="sxs-lookup"><span data-stu-id="489d9-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="489d9-109">從 Windows Server 2003 開始，此原則的預設值為1。</span><span class="sxs-lookup"><span data-stu-id="489d9-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="489d9-110">設定此原則時， [維護安裝](maintenance-installation.md) 只能使用來自受保護快取的轉換。</span><span class="sxs-lookup"><span data-stu-id="489d9-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="489d9-111">當安裝程式發現本機電腦上缺少轉換時，安裝程式會嘗試還原轉換。</span><span class="sxs-lookup"><span data-stu-id="489d9-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="489d9-112">為了讓安裝程式還原轉換，安全轉換必須位於安裝套件來源清單中的授權來源。</span><span class="sxs-lookup"><span data-stu-id="489d9-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="489d9-113">如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="489d9-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="489d9-114">如果轉換無法使用或無法載入，維護安裝將會失敗。</span><span class="sxs-lookup"><span data-stu-id="489d9-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="489d9-115">在 Windows Server 2003 上，如果未設定此原則，預設行為是將轉換儲存在安全的位置。</span><span class="sxs-lookup"><span data-stu-id="489d9-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="489d9-116">在 Windows Server 2003 之前的所有版本上，如果未設定此原則，則預設行為是在使用者設定檔中儲存轉換。</span><span class="sxs-lookup"><span data-stu-id="489d9-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="489d9-117">如需詳細資訊，請參閱 [安全的轉換](secured-transforms.md) 。</span><span class="sxs-lookup"><span data-stu-id="489d9-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="489d9-118">Windows Installer 會將 [TransformsAtSource 原則](transformsatsource-policy.md) 解釋為與 TransformsSecure 原則相同的原則。</span><span class="sxs-lookup"><span data-stu-id="489d9-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="489d9-119">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="489d9-119">Registry Key</span></span>

<span data-ttu-id="489d9-120">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="489d9-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="489d9-121">資料類型</span><span class="sxs-lookup"><span data-stu-id="489d9-121">Data Type</span></span>

<span data-ttu-id="489d9-122">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="489d9-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="489d9-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="489d9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="489d9-124">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="489d9-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



