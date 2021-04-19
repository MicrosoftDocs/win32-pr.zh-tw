---
description: 安裝程式會將 SystemFolder 屬性設定為系統資料夾的完整路徑。
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985778"
---
# <a name="systemfolder-property"></a><span data-ttu-id="cef1a-103">SystemFolder 屬性</span><span class="sxs-lookup"><span data-stu-id="cef1a-103">SystemFolder property</span></span>

<span data-ttu-id="cef1a-104">安裝程式會將 **SystemFolder** 屬性設定為系統資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cef1a-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="cef1a-105">備註</span><span class="sxs-lookup"><span data-stu-id="cef1a-105">Remarks</span></span>

<span data-ttu-id="cef1a-106">安裝程式會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="cef1a-106">The installer sets this property.</span></span> <span data-ttu-id="cef1a-107">例如，在32位 Windows 上，值可能是 C： \\ Windows \\ System32。</span><span class="sxs-lookup"><span data-stu-id="cef1a-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="cef1a-108">在64位的 Windows 上，此值可能是 C： \\ Windows \\ SysWow64。</span><span class="sxs-lookup"><span data-stu-id="cef1a-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="cef1a-109">此資料夾通常是 Windows 資料夾的子目錄。</span><span class="sxs-lookup"><span data-stu-id="cef1a-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="cef1a-110">不過，它會在設定共用視窗時位於伺服器上。</span><span class="sxs-lookup"><span data-stu-id="cef1a-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="cef1a-111">這是本機資料夾，即使是針對共用視窗進行設定亦同。</span><span class="sxs-lookup"><span data-stu-id="cef1a-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef1a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cef1a-112">Requirements</span></span>



| <span data-ttu-id="cef1a-113">需求</span><span class="sxs-lookup"><span data-stu-id="cef1a-113">Requirement</span></span> | <span data-ttu-id="cef1a-114">值</span><span class="sxs-lookup"><span data-stu-id="cef1a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef1a-115">版本</span><span class="sxs-lookup"><span data-stu-id="cef1a-115">Version</span></span><br/> | <span data-ttu-id="cef1a-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="cef1a-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cef1a-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="cef1a-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cef1a-118">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="cef1a-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cef1a-119">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="cef1a-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cef1a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cef1a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef1a-121">屬性</span><span class="sxs-lookup"><span data-stu-id="cef1a-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




