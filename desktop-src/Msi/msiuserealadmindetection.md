---
description: 將 MSIUSEREALADMINDETECTION 屬性設定為1，以要求安裝程式在設定 AdminUser 屬性時，使用實際的使用者資訊。
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: MSIUSEREALADMINDETECTION 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995995"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="4b4b8-103">MSIUSEREALADMINDETECTION 屬性</span><span class="sxs-lookup"><span data-stu-id="4b4b8-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="4b4b8-104">將 **MSIUSEREALADMINDETECTION** 屬性設定為1，以要求安裝程式在設定 [**AdminUser**](adminuser.md) 屬性時，使用實際的使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="4b4b8-105">在 Windows Vista 上執行時，特殊 [**許可權**](privileged.md) 和 **AdminUser** 相同。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="4b4b8-106">作者應該在新的封裝中使用具有特殊 **許可權** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="4b4b8-107">需要特殊 **許可權** 和 **AdminUser** 屬性的舊版封裝，可以藉由設定 **MSIUSEREALADMINDETECTION** 屬性來還原差異。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4b8-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b4b8-108">Requirements</span></span>



| <span data-ttu-id="4b4b8-109">需求</span><span class="sxs-lookup"><span data-stu-id="4b4b8-109">Requirement</span></span> | <span data-ttu-id="4b4b8-110">值</span><span class="sxs-lookup"><span data-stu-id="4b4b8-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4b8-111">版本</span><span class="sxs-lookup"><span data-stu-id="4b4b8-111">Version</span></span><br/> | <span data-ttu-id="4b4b8-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4b4b8-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4b4b8-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="4b4b8-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b4b8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b4b8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4b8-116">屬性</span><span class="sxs-lookup"><span data-stu-id="4b4b8-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4b4b8-117">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="4b4b8-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




