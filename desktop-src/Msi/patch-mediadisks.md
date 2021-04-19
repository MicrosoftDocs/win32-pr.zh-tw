---
description: MediaDisks 屬性會列舉此產品實例的所有媒體磁片。 這個屬性會呼叫 MsiSourceListEnumMediaDisks。 以記錄物件的陣列形式傳回磁片資訊。
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: MediaDisks 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992141"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="039cd-105">MediaDisks 屬性</span><span class="sxs-lookup"><span data-stu-id="039cd-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="039cd-106">**MediaDisks** 屬性會列舉此產品實例的所有媒體磁片。</span><span class="sxs-lookup"><span data-stu-id="039cd-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="039cd-107">這個屬性會呼叫 [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)。</span><span class="sxs-lookup"><span data-stu-id="039cd-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="039cd-108">以 [**記錄**](record-object.md) 物件的陣列形式傳回磁片資訊。</span><span class="sxs-lookup"><span data-stu-id="039cd-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="039cd-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="039cd-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="039cd-110">語法</span><span class="sxs-lookup"><span data-stu-id="039cd-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="039cd-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="039cd-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="039cd-112">備註</span><span class="sxs-lookup"><span data-stu-id="039cd-112">Remarks</span></span>

<span data-ttu-id="039cd-113">在每個記錄中，第一個欄位包含磁片識別碼，第二個欄位包含磁片區標籤，而第三個欄位包含為磁片註冊的磁片提示。</span><span class="sxs-lookup"><span data-stu-id="039cd-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="039cd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="039cd-114">Requirements</span></span>



| <span data-ttu-id="039cd-115">需求</span><span class="sxs-lookup"><span data-stu-id="039cd-115">Requirement</span></span> | <span data-ttu-id="039cd-116">值</span><span class="sxs-lookup"><span data-stu-id="039cd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="039cd-117">版本</span><span class="sxs-lookup"><span data-stu-id="039cd-117">Version</span></span><br/> | <span data-ttu-id="039cd-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="039cd-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="039cd-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="039cd-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="039cd-120">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="039cd-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="039cd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="039cd-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="039cd-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="039cd-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="039cd-123">IID</span><span class="sxs-lookup"><span data-stu-id="039cd-123">IID</span></span><br/>     | <span data-ttu-id="039cd-124">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="039cd-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="039cd-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="039cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039cd-126">**Patch**</span><span class="sxs-lookup"><span data-stu-id="039cd-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="039cd-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="039cd-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="039cd-128">**Record**</span><span class="sxs-lookup"><span data-stu-id="039cd-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="039cd-129">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="039cd-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




