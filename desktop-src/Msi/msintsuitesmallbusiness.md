---
description: 在 Windows 2000 和更新版本的作業系統上，如果已安裝 Microsoft Small Business Server，安裝程式會將 MsiNTSuiteSmallBusiness 屬性設定為1。
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: MsiNTSuiteSmallBusiness 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976039"
---
# <a name="msintsuitesmallbusiness-property"></a><span data-ttu-id="5c73c-103">MsiNTSuiteSmallBusiness 屬性</span><span class="sxs-lookup"><span data-stu-id="5c73c-103">MsiNTSuiteSmallBusiness property</span></span>

<span data-ttu-id="5c73c-104">在 Windows 2000 和更新版本的作業系統上，如果已安裝 Microsoft Small Business Server，安裝程式會將 **MsiNTSuiteSmallBusiness** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="5c73c-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusiness** property to 1 if Microsoft Small Business Server is installed.</span></span> <span data-ttu-id="5c73c-105">只有在 \_ \_ [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中設定了 VER SUITE SMALLBUSINESS 旗標時，安裝程式才會將這個屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="5c73c-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="5c73c-106">否則，安裝程式不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5c73c-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c73c-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c73c-107">Requirements</span></span>



| <span data-ttu-id="5c73c-108">需求</span><span class="sxs-lookup"><span data-stu-id="5c73c-108">Requirement</span></span> | <span data-ttu-id="5c73c-109">值</span><span class="sxs-lookup"><span data-stu-id="5c73c-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c73c-110">版本</span><span class="sxs-lookup"><span data-stu-id="5c73c-110">Version</span></span><br/> | <span data-ttu-id="5c73c-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5c73c-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5c73c-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5c73c-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5c73c-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="5c73c-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5c73c-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="5c73c-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c73c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c73c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c73c-116">屬性</span><span class="sxs-lookup"><span data-stu-id="5c73c-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
