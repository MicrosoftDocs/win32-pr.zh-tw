---
description: ProductVersion 屬性的值是字串格式的產品版本。
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996405"
---
# <a name="productversion-property"></a><span data-ttu-id="b3c85-103">ProductVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="b3c85-103">ProductVersion property</span></span>

<span data-ttu-id="b3c85-104">**ProductVersion** 屬性的值是字串格式的產品版本。</span><span class="sxs-lookup"><span data-stu-id="b3c85-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="b3c85-105">此為必要屬性。</span><span class="sxs-lookup"><span data-stu-id="b3c85-105">This property is REQUIRED.</span></span>

<span data-ttu-id="b3c85-106">字串的格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="b3c85-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="b3c85-107">major.minor.build</span><span class="sxs-lookup"><span data-stu-id="b3c85-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="b3c85-108">第一個欄位是主要版本，最大值為255。</span><span class="sxs-lookup"><span data-stu-id="b3c85-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="b3c85-109">第二個欄位是次要版本，最大值為255。</span><span class="sxs-lookup"><span data-stu-id="b3c85-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="b3c85-110">第三個欄位稱為組建版本或更新版本，且最大值為65535。</span><span class="sxs-lookup"><span data-stu-id="b3c85-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c85-111">備註</span><span class="sxs-lookup"><span data-stu-id="b3c85-111">Remarks</span></span>

<span data-ttu-id="b3c85-112">**ProductVersion** 的三個欄位中至少有一個必須變更，才能使用 [升級資料表](upgrade-table.md)進行升級。</span><span class="sxs-lookup"><span data-stu-id="b3c85-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="b3c85-113">只要變更封裝程式碼，但不變更 **ProductVersion** 和 [**ProductCode**](productcode.md) 的更新，就稱為 [小型更新](small-updates.md)。</span><span class="sxs-lookup"><span data-stu-id="b3c85-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="b3c85-114">提供的三個版本欄位主要是為了方便起見。</span><span class="sxs-lookup"><span data-stu-id="b3c85-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="b3c85-115">例如，如果您想要變更 **ProductVersion**，但不想變更主要或次要版本，您可以變更組建版本。</span><span class="sxs-lookup"><span data-stu-id="b3c85-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="b3c85-116">請注意，Windows Installer 只會使用產品版本的前三個欄位。</span><span class="sxs-lookup"><span data-stu-id="b3c85-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="b3c85-117">如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。</span><span class="sxs-lookup"><span data-stu-id="b3c85-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c85-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3c85-118">Requirements</span></span>



| <span data-ttu-id="b3c85-119">需求</span><span class="sxs-lookup"><span data-stu-id="b3c85-119">Requirement</span></span> | <span data-ttu-id="b3c85-120">值</span><span class="sxs-lookup"><span data-stu-id="b3c85-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c85-121">版本</span><span class="sxs-lookup"><span data-stu-id="b3c85-121">Version</span></span><br/> | <span data-ttu-id="b3c85-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b3c85-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b3c85-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b3c85-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b3c85-124">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="b3c85-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b3c85-125">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="b3c85-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3c85-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3c85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c85-127">屬性</span><span class="sxs-lookup"><span data-stu-id="b3c85-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="b3c85-128">修補和升級</span><span class="sxs-lookup"><span data-stu-id="b3c85-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="b3c85-129">small update</span><span class="sxs-lookup"><span data-stu-id="b3c85-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




