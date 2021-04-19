---
title: 核心模式驅動程式的安全開機功能簽署需求
description: 核心模式驅動程式的安全開機功能簽署需求
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106993736"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="64776-103">核心模式驅動程式的安全開機功能簽署需求</span><span class="sxs-lookup"><span data-stu-id="64776-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="64776-104">平台</span><span class="sxs-lookup"><span data-stu-id="64776-104">Platforms</span></span>

<span data-ttu-id="64776-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="64776-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="64776-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64776-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="64776-107">Description</span><span class="sxs-lookup"><span data-stu-id="64776-107">Description</span></span>

<span data-ttu-id="64776-108">在 Windows 8 和 Windows Server 2012 （包括 WinPE）中，核心已被鎖定，以防止開機或根套件所引進的惡意程式碼規避簽署驅動程式的 Windows 作業系統安全性需求。</span><span class="sxs-lookup"><span data-stu-id="64776-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="64776-109">此變更會影響支援整合可延伸韌體介面之裝置的所有核心模式驅動程式 (UEFI) 安全開機;Windows 8 用戶端電腦的認證，以及伺服器的選擇性選項，都需要 UEFI 安全開機。</span><span class="sxs-lookup"><span data-stu-id="64776-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="64776-110">它不會影響使用者模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="64776-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="64776-111">核心模式驅動程式的標準開發牽涉到使用核心模式的偵錯工具或開機設定資料 (BCD) <testsigning> 設定。</span><span class="sxs-lookup"><span data-stu-id="64776-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="64776-112">開啟安全開機時，這兩個都是停用的。</span><span class="sxs-lookup"><span data-stu-id="64776-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="64776-113">表現</span><span class="sxs-lookup"><span data-stu-id="64776-113">Manifestation</span></span>

<span data-ttu-id="64776-114">如果不是由受信任的憑證授權單位單位 (CA) 正確簽署，就不會執行核心模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="64776-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="64776-115">作業系統將不會允許不受信任的驅動程式執行，而且不允許使用標準機制，例如內核偵錯工具和 testsigning。</span><span class="sxs-lookup"><span data-stu-id="64776-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="64776-116">降低</span><span class="sxs-lookup"><span data-stu-id="64776-116">Mitigation</span></span>

<span data-ttu-id="64776-117">若要測試驅動程式，您必須停用 BIOS 中的安全開機，並符合其他測試簽署需求 (請參閱以下) 。</span><span class="sxs-lookup"><span data-stu-id="64776-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="64776-118">更廣泛地散發驅動程式時，必須由受信任的 CA 正確簽署。</span><span class="sxs-lookup"><span data-stu-id="64776-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="64776-119">資源</span><span class="sxs-lookup"><span data-stu-id="64776-119">Resources</span></span>

-   <span data-ttu-id="64776-120">[簽署驅動程式](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64776-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 