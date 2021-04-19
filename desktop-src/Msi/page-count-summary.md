---
description: '[頁面計數摘要] 屬性包含安裝套件所需的最低安裝程式版本。'
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: 頁面計數摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996188"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="05a46-103">頁面計數摘要屬性</span><span class="sxs-lookup"><span data-stu-id="05a46-103">Page Count Summary property</span></span>

<span data-ttu-id="05a46-104">[ **頁面計數摘要** ] 屬性包含安裝套件所需的最低安裝程式版本。</span><span class="sxs-lookup"><span data-stu-id="05a46-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="05a46-105">至少要有 Windows Installer 2.0，這個屬性必須設定為整數200。</span><span class="sxs-lookup"><span data-stu-id="05a46-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="05a46-106">至少要有 Windows Installer 3.0，這個屬性必須設定為整數300。</span><span class="sxs-lookup"><span data-stu-id="05a46-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="05a46-107">至少要有 Windows Installer 3.1，這個屬性必須設定為301。</span><span class="sxs-lookup"><span data-stu-id="05a46-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="05a46-108">至少要有 Windows Installer 4.5，這個屬性必須設定為405。</span><span class="sxs-lookup"><span data-stu-id="05a46-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="05a46-109">至少要有 Windows Installer 5.0，這個屬性必須設定為500。</span><span class="sxs-lookup"><span data-stu-id="05a46-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="05a46-110">若為 [64 位 Windows Installer 套件](64-bit-windows-installer-packages.md)，這個屬性必須設定為整數200或更高的整數。</span><span class="sxs-lookup"><span data-stu-id="05a46-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="05a46-111">若為 Arm64 平臺上的64位 Windows Installer 套件，這個屬性必須設定為整數500或更高的整數。</span><span class="sxs-lookup"><span data-stu-id="05a46-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="05a46-112">若為轉換封裝，[ **頁面計數摘要** ] 屬性會包含處理轉換所需的最低安裝程式版本。</span><span class="sxs-lookup"><span data-stu-id="05a46-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="05a46-113">設定為兩個 **頁面計數摘要** 屬性值的最大值，這些值屬於用來產生轉換的資料庫。</span><span class="sxs-lookup"><span data-stu-id="05a46-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="05a46-114">針對 patch 封裝，[ **頁面計數摘要** ] 屬性會設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="05a46-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="05a46-115">這是必要的摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="05a46-115">This summary property is required.</span></span>

<span data-ttu-id="05a46-116">這個屬性可用來撰寫只能由指定的最小或更新版本 Windows Installer 安裝的封裝。</span><span class="sxs-lookup"><span data-stu-id="05a46-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a46-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="05a46-117">Requirements</span></span>



| <span data-ttu-id="05a46-118">需求</span><span class="sxs-lookup"><span data-stu-id="05a46-118">Requirement</span></span> | <span data-ttu-id="05a46-119">值</span><span class="sxs-lookup"><span data-stu-id="05a46-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a46-120">版本</span><span class="sxs-lookup"><span data-stu-id="05a46-120">Version</span></span><br/> | <span data-ttu-id="05a46-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="05a46-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05a46-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="05a46-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05a46-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="05a46-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05a46-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05a46-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a46-125">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="05a46-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




