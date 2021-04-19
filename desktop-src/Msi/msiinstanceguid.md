---
description: MSIINSTANCEGUID 屬性的存在指出產品程式碼&\# 8211; 變更轉換會向產品註冊。
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: MSIINSTANCEGUID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982538"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="97a11-103">MSIINSTANCEGUID 屬性</span><span class="sxs-lookup"><span data-stu-id="97a11-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="97a11-104">**MSIINSTANCEGUID** 屬性的存在指出產品程式碼-變更轉換已註冊至產品。</span><span class="sxs-lookup"><span data-stu-id="97a11-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="97a11-105">**MSIINSTANCEGUID** 屬性的值會指定要用來安裝產品的哪一個實例。</span><span class="sxs-lookup"><span data-stu-id="97a11-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="97a11-106">**MSIINSTANCEGUID** 屬性只能參考已經隨實例轉換安裝的產品。</span><span class="sxs-lookup"><span data-stu-id="97a11-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="97a11-107">實例轉換是在 Windows Server 2003 或 Windows XP 上執行的安裝程式所提供的產品代碼變更轉換。</span><span class="sxs-lookup"><span data-stu-id="97a11-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="97a11-108">如需詳細資訊，請參閱 [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="97a11-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97a11-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="97a11-109">Requirements</span></span>



| <span data-ttu-id="97a11-110">需求</span><span class="sxs-lookup"><span data-stu-id="97a11-110">Requirement</span></span> | <span data-ttu-id="97a11-111">值</span><span class="sxs-lookup"><span data-stu-id="97a11-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a11-112">版本</span><span class="sxs-lookup"><span data-stu-id="97a11-112">Version</span></span><br/> | <span data-ttu-id="97a11-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="97a11-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97a11-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="97a11-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97a11-115">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="97a11-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="97a11-116">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="97a11-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97a11-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97a11-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a11-118">屬性</span><span class="sxs-lookup"><span data-stu-id="97a11-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="97a11-119">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="97a11-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




