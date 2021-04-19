---
description: 您可以設定 MSIDEPLOYMENTCOMPLIANT 屬性，向安裝程式指出封裝已撰寫並測試，以符合 Windows Vista (UAC) 的使用者帳戶控制。
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: MSIDEPLOYMENTCOMPLIANT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994343"
---
# <a name="msideploymentcompliant-property"></a><span data-ttu-id="f19db-103">MSIDEPLOYMENTCOMPLIANT 屬性</span><span class="sxs-lookup"><span data-stu-id="f19db-103">MSIDEPLOYMENTCOMPLIANT property</span></span>

<span data-ttu-id="f19db-104">您可以設定 **MSIDEPLOYMENTCOMPLIANT** 屬性，向安裝程式指出封裝已撰寫並測試，以符合 Windows VISTA (UAC) 的 [*使用者帳戶控制*](u-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="f19db-104">The **MSIDEPLOYMENTCOMPLIANT** property can be set to indicate to the installer that the package has been authored and tested to comply with [*User Account Control*](u-gly.md) (UAC) in Windows Vista.</span></span> <span data-ttu-id="f19db-105">如果未設定此屬性，安裝程式會判斷套件是否符合 Windows Vista 上的 UAC。</span><span class="sxs-lookup"><span data-stu-id="f19db-105">If this property is not set, the installer will determine whether the package complies with UAC on Windows Vista.</span></span>

<span data-ttu-id="f19db-106">如需 UAC 和 Windows Installer 的詳細資訊，請參閱 [使用 Windows Installer 搭配 uac](using-windows-installer-with-uac.md) 和 [套件的指導方針](guidelines-for-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="f19db-106">For more information about UAC and Windows Installer, see [Using Windows Installer with UAC](using-windows-installer-with-uac.md) and [Guidelines for Packages](guidelines-for-packages.md).</span></span>

<span data-ttu-id="f19db-107">**Windows Installer 3.1、Windows Installer 3.0 和 Windows Installer 2.0：** 忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f19db-107">**Windows Installer 3.1, Windows Installer 3.0 and Windows Installer 2.0:** This property is ignored.</span></span> <span data-ttu-id="f19db-108">只有 Windows Vista 中的 Windows Installer 4.0 才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f19db-108">This property is only used by Windows Installer 4.0 in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19db-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="f19db-109">Requirements</span></span>



| <span data-ttu-id="f19db-110">需求</span><span class="sxs-lookup"><span data-stu-id="f19db-110">Requirement</span></span> | <span data-ttu-id="f19db-111">值</span><span class="sxs-lookup"><span data-stu-id="f19db-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19db-112">版本</span><span class="sxs-lookup"><span data-stu-id="f19db-112">Version</span></span><br/> | <span data-ttu-id="f19db-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f19db-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f19db-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f19db-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f19db-115">如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="f19db-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f19db-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f19db-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19db-117">屬性</span><span class="sxs-lookup"><span data-stu-id="f19db-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="f19db-118">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="f19db-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




