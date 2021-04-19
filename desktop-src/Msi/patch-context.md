---
description: CoNtext 屬性會傳回此修補程式的內容。
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch。 CoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982511"
---
# <a name="patchcontext-property"></a><span data-ttu-id="c2b25-103">Patch。 CoNtext 屬性</span><span class="sxs-lookup"><span data-stu-id="c2b25-103">Patch.Context property</span></span>

<span data-ttu-id="c2b25-104">**CoNtext** 屬性會傳回此修補程式的內容。</span><span class="sxs-lookup"><span data-stu-id="c2b25-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="c2b25-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c2b25-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b25-106">語法</span><span class="sxs-lookup"><span data-stu-id="c2b25-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="c2b25-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="c2b25-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c2b25-108">備註</span><span class="sxs-lookup"><span data-stu-id="c2b25-108">Remarks</span></span>

<span data-ttu-id="c2b25-109">這個屬性會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c2b25-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="c2b25-110">Context</span><span class="sxs-lookup"><span data-stu-id="c2b25-110">Context</span></span>                        | <span data-ttu-id="c2b25-111">值</span><span class="sxs-lookup"><span data-stu-id="c2b25-111">Value</span></span> | <span data-ttu-id="c2b25-112">意義</span><span class="sxs-lookup"><span data-stu-id="c2b25-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="c2b25-113">MSIINSTALLCONTEXT \_ USERMANAGED</span><span class="sxs-lookup"><span data-stu-id="c2b25-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="c2b25-114">1</span><span class="sxs-lookup"><span data-stu-id="c2b25-114">1</span></span>     | <span data-ttu-id="c2b25-115">在受控內容下修補。</span><span class="sxs-lookup"><span data-stu-id="c2b25-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="c2b25-116">MSIINSTALLCONTEXT \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="c2b25-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="c2b25-117">2</span><span class="sxs-lookup"><span data-stu-id="c2b25-117">2</span></span>     | <span data-ttu-id="c2b25-118">在未受管理的內容下修補。</span><span class="sxs-lookup"><span data-stu-id="c2b25-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="c2b25-119">MSIINSTALLCONTEXT \_ 機器</span><span class="sxs-lookup"><span data-stu-id="c2b25-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="c2b25-120">4</span><span class="sxs-lookup"><span data-stu-id="c2b25-120">4</span></span>     | <span data-ttu-id="c2b25-121">電腦內容下的修補程式。</span><span class="sxs-lookup"><span data-stu-id="c2b25-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="c2b25-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2b25-122">Requirements</span></span>



| <span data-ttu-id="c2b25-123">需求</span><span class="sxs-lookup"><span data-stu-id="c2b25-123">Requirement</span></span> | <span data-ttu-id="c2b25-124">值</span><span class="sxs-lookup"><span data-stu-id="c2b25-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b25-125">版本</span><span class="sxs-lookup"><span data-stu-id="c2b25-125">Version</span></span><br/> | <span data-ttu-id="c2b25-126">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c2b25-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c2b25-127">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c2b25-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c2b25-128">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c2b25-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c2b25-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c2b25-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c2b25-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b25-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c2b25-131">IID</span><span class="sxs-lookup"><span data-stu-id="c2b25-131">IID</span></span><br/>     | <span data-ttu-id="c2b25-132">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c2b25-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="c2b25-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2b25-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b25-134">**Patch 物件**</span><span class="sxs-lookup"><span data-stu-id="c2b25-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="c2b25-135">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="c2b25-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




