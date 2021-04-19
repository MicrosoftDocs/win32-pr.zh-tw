---
description: 在 Windows XP 和更新版本的作業系統上，如果作業系統是 Windows XP Home Edition，安裝程式會將 MsiNTSuitePersonal 屬性設定為1。
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: MsiNTSuitePersonal 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001815"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="d28f7-103">MsiNTSuitePersonal 屬性</span><span class="sxs-lookup"><span data-stu-id="d28f7-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="d28f7-104">在 Windows XP 和更新版本的作業系統上，如果作業系統是 Windows XP Home Edition，安裝程式會將 **MsiNTSuitePersonal** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="d28f7-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="d28f7-105">只有在 \_ \_ [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中設定了 VER SUITE 個人旗標時，安裝程式才會將這個屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="d28f7-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="d28f7-106">否則，安裝程式不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d28f7-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d28f7-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="d28f7-107">Requirements</span></span>



| <span data-ttu-id="d28f7-108">需求</span><span class="sxs-lookup"><span data-stu-id="d28f7-108">Requirement</span></span> | <span data-ttu-id="d28f7-109">值</span><span class="sxs-lookup"><span data-stu-id="d28f7-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d28f7-110">版本</span><span class="sxs-lookup"><span data-stu-id="d28f7-110">Version</span></span><br/> | <span data-ttu-id="d28f7-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d28f7-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d28f7-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d28f7-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d28f7-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d28f7-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d28f7-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d28f7-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d28f7-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d28f7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d28f7-116">屬性</span><span class="sxs-lookup"><span data-stu-id="d28f7-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
