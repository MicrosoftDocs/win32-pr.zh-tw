---
description: 如果使用者具有系統管理員許可權，則安裝程式會設定此屬性。
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999741"
---
# <a name="adminuser-property"></a><span data-ttu-id="ace19-103">AdminUser 屬性</span><span class="sxs-lookup"><span data-stu-id="ace19-103">AdminUser property</span></span>

<span data-ttu-id="ace19-104">如果使用者具有系統管理員許可權，則安裝程式會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ace19-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="ace19-105">**Windows Server 2008 和 Windows Vista：\*\*\*\*AdminUser** 屬性與具有特殊 [**許可權**](privileged.md)的屬性相同。</span><span class="sxs-lookup"><span data-stu-id="ace19-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="ace19-106">作者應該使用具特殊 **許可權** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="ace19-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="ace19-107">如果使用者具有系統管理員許可權、系統管理員已指派應用程式，或使用者和電腦原則 AlwaysInstallElevated 都設定為 true，則安裝程式會設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ace19-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace19-108">備註</span><span class="sxs-lookup"><span data-stu-id="ace19-108">Remarks</span></span>

<span data-ttu-id="ace19-109">這些屬性之間的差異可能已用於某些舊版封裝中。</span><span class="sxs-lookup"><span data-stu-id="ace19-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="ace19-110">例如， **AdminUser** 可能已在條件陳述式中使用，而不是特殊 [**許可權**](privileged.md) ，因為如果使用者是系統管理員，則安裝程式只會設定 **AdminUser** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ace19-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="ace19-111">如果使用者是系統管理員，或原則可讓使用者以較高的許可權安裝，則安裝程式會設定具有 **特殊許可權的屬性。**</span><span class="sxs-lookup"><span data-stu-id="ace19-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="ace19-112">**Windows Server 2008 和 Windows Vista：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="ace19-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="ace19-113">具有特殊 [**許可權**](privileged.md) 的和 **AdminUser** 相同。</span><span class="sxs-lookup"><span data-stu-id="ace19-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="ace19-114">需要特殊 **許可權** 和 **AdminUser** 屬性的封裝，可以藉由設定 [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) 屬性來還原差異。</span><span class="sxs-lookup"><span data-stu-id="ace19-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="ace19-115">如需詳細資訊，請參閱以 [較高的許可權針對非系統管理員](installing-a-package-with-elevated-privileges-for-a-non-admin.md)和具 [**特殊許可權**](privileged.md) 的屬性安裝套件。</span><span class="sxs-lookup"><span data-stu-id="ace19-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace19-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ace19-116">Requirements</span></span>



| <span data-ttu-id="ace19-117">需求</span><span class="sxs-lookup"><span data-stu-id="ace19-117">Requirement</span></span> | <span data-ttu-id="ace19-118">值</span><span class="sxs-lookup"><span data-stu-id="ace19-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace19-119">版本</span><span class="sxs-lookup"><span data-stu-id="ace19-119">Version</span></span><br/> | <span data-ttu-id="ace19-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ace19-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ace19-121">Windows Vista 或 Windows Server 2008 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ace19-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="ace19-122">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="ace19-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ace19-123">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="ace19-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ace19-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ace19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace19-125">屬性</span><span class="sxs-lookup"><span data-stu-id="ace19-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




