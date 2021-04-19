---
description: 在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows 2000 Advanced Server，安裝程式會將 MsiNTSuiteEnterprise 屬性設定為1。
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: MsiNTSuiteEnterprise 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992807"
---
# <a name="msintsuiteenterprise-property"></a><span data-ttu-id="62b87-103">MsiNTSuiteEnterprise 屬性</span><span class="sxs-lookup"><span data-stu-id="62b87-103">MsiNTSuiteEnterprise property</span></span>

<span data-ttu-id="62b87-104">在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows 2000 Advanced Server，安裝程式會將 **MsiNTSuiteEnterprise** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="62b87-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteEnterprise** property to 1 if Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="62b87-105">只有當 VER \_ SUITE \_ ENTERPRISE 旗標設定于 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中時，安裝程式才會將這個屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="62b87-105">The installer sets this property to 1 only if the VER\_SUITE\_ENTERPRISE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="62b87-106">否則，安裝程式不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="62b87-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b87-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="62b87-107">Requirements</span></span>



| <span data-ttu-id="62b87-108">需求</span><span class="sxs-lookup"><span data-stu-id="62b87-108">Requirement</span></span> | <span data-ttu-id="62b87-109">值</span><span class="sxs-lookup"><span data-stu-id="62b87-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b87-110">版本</span><span class="sxs-lookup"><span data-stu-id="62b87-110">Version</span></span><br/> | <span data-ttu-id="62b87-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="62b87-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62b87-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="62b87-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62b87-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="62b87-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="62b87-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="62b87-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62b87-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62b87-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b87-116">屬性</span><span class="sxs-lookup"><span data-stu-id="62b87-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
