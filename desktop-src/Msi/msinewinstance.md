---
description: MSINEWINSTANCE 屬性工作表示安裝具有實例轉換之產品的新實例。
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: MSINEWINSTANCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987856"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="daf00-103">MSINEWINSTANCE 屬性</span><span class="sxs-lookup"><span data-stu-id="daf00-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="daf00-104">**MSINEWINSTANCE** 屬性工作表示安裝具有實例轉換之產品的新實例。</span><span class="sxs-lookup"><span data-stu-id="daf00-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="daf00-105">這個屬性會透過產品程式碼來支援多個實例–變更轉換。</span><span class="sxs-lookup"><span data-stu-id="daf00-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="daf00-106">這個屬性的值為1。</span><span class="sxs-lookup"><span data-stu-id="daf00-106">The value of this property is 1.</span></span> <span data-ttu-id="daf00-107">在命令列上存在此屬性時，必須同時存在 [**轉換**](transforms.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="daf00-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="daf00-108">**轉換** 中所列的第一個轉換必須是實例轉換。</span><span class="sxs-lookup"><span data-stu-id="daf00-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="daf00-109">如需詳細資訊，請參閱 [安裝產品和修補程式的多個實例](installing-multiple-instances-of-products-and-patches.md)</span><span class="sxs-lookup"><span data-stu-id="daf00-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="daf00-110">在 Windows Server 2003 或 Windows XP 中執行系統的安裝程式可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="daf00-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf00-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="daf00-111">Requirements</span></span>



| <span data-ttu-id="daf00-112">需求</span><span class="sxs-lookup"><span data-stu-id="daf00-112">Requirement</span></span> | <span data-ttu-id="daf00-113">值</span><span class="sxs-lookup"><span data-stu-id="daf00-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf00-114">版本</span><span class="sxs-lookup"><span data-stu-id="daf00-114">Version</span></span><br/> | <span data-ttu-id="daf00-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="daf00-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="daf00-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="daf00-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="daf00-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="daf00-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="daf00-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="daf00-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="daf00-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="daf00-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf00-120">屬性</span><span class="sxs-lookup"><span data-stu-id="daf00-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="daf00-121">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="daf00-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




