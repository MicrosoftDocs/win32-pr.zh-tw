---
description: 在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows 2000 Datacenter Server，安裝程式會將 MsiNTSuiteDataCenter 屬性設定為1。
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: MsiNTSuiteDataCenter 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987839"
---
# <a name="msintsuitedatacenter-property"></a><span data-ttu-id="30b17-103">MsiNTSuiteDataCenter 屬性</span><span class="sxs-lookup"><span data-stu-id="30b17-103">MsiNTSuiteDataCenter property</span></span>

<span data-ttu-id="30b17-104">在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows 2000 Datacenter Server，安裝程式會將 **MsiNTSuiteDataCenter** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="30b17-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteDataCenter** property to 1 if Windows 2000 Datacenter Server is installed.</span></span> <span data-ttu-id="30b17-105">只有當 VER \_ SUITE \_ DATACENTER 旗標設定于 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中時，安裝程式才會將這個屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="30b17-105">The installer sets this property to 1 only if the VER\_SUITE\_DATACENTER flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="30b17-106">否則，安裝程式不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="30b17-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b17-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="30b17-107">Requirements</span></span>



| <span data-ttu-id="30b17-108">需求</span><span class="sxs-lookup"><span data-stu-id="30b17-108">Requirement</span></span> | <span data-ttu-id="30b17-109">值</span><span class="sxs-lookup"><span data-stu-id="30b17-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b17-110">版本</span><span class="sxs-lookup"><span data-stu-id="30b17-110">Version</span></span><br/> | <span data-ttu-id="30b17-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="30b17-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30b17-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="30b17-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="30b17-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="30b17-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="30b17-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="30b17-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30b17-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30b17-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b17-116">屬性</span><span class="sxs-lookup"><span data-stu-id="30b17-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
