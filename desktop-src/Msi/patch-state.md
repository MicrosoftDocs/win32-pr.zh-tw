---
description: State 屬性會傳回這個 patch 實例的安裝狀態。
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch。 State 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979547"
---
# <a name="patchstate-property"></a><span data-ttu-id="91031-103">Patch。 State 屬性</span><span class="sxs-lookup"><span data-stu-id="91031-103">Patch.State property</span></span>

<span data-ttu-id="91031-104">**State** 屬性會傳回這個 patch 實例的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="91031-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="91031-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="91031-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="91031-106">語法</span><span class="sxs-lookup"><span data-stu-id="91031-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="91031-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="91031-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="91031-108">備註</span><span class="sxs-lookup"><span data-stu-id="91031-108">Remarks</span></span>

<span data-ttu-id="91031-109">這個屬性會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="91031-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="91031-110">安裝狀態</span><span class="sxs-lookup"><span data-stu-id="91031-110">Installation State</span></span>        | <span data-ttu-id="91031-111">意義</span><span class="sxs-lookup"><span data-stu-id="91031-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="91031-112">套用 \_ 的 MSIPATCHSTATE</span><span class="sxs-lookup"><span data-stu-id="91031-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="91031-113">Patch 會套用至此產品實例。</span><span class="sxs-lookup"><span data-stu-id="91031-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="91031-114">MSIPATCHSTATE 已被 \_ 取代</span><span class="sxs-lookup"><span data-stu-id="91031-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="91031-115">Patch 已套用至此產品實例，但已被取代。</span><span class="sxs-lookup"><span data-stu-id="91031-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="91031-116">MSIPATCHSTATE 已 \_ 過時</span><span class="sxs-lookup"><span data-stu-id="91031-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="91031-117">Patch 已套用於此產品實例，但已淘汰。</span><span class="sxs-lookup"><span data-stu-id="91031-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="91031-118">\_ \_ 如果 [**修補程式**](patch-object.md)物件是以空字串來初始化， 則這個方法可能會傳回錯誤未知的修補程式。</span><span class="sxs-lookup"><span data-stu-id="91031-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="91031-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="91031-119">Requirements</span></span>



| <span data-ttu-id="91031-120">需求</span><span class="sxs-lookup"><span data-stu-id="91031-120">Requirement</span></span> | <span data-ttu-id="91031-121">值</span><span class="sxs-lookup"><span data-stu-id="91031-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91031-122">版本</span><span class="sxs-lookup"><span data-stu-id="91031-122">Version</span></span><br/> | <span data-ttu-id="91031-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="91031-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="91031-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="91031-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="91031-125">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="91031-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="91031-126">DLL</span><span class="sxs-lookup"><span data-stu-id="91031-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="91031-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91031-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="91031-128">IID</span><span class="sxs-lookup"><span data-stu-id="91031-128">IID</span></span><br/>     | <span data-ttu-id="91031-129">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="91031-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="91031-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91031-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91031-131">**Patch**</span><span class="sxs-lookup"><span data-stu-id="91031-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="91031-132">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="91031-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="91031-133">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="91031-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




