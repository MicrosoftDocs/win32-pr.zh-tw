---
description: MediaDisks 屬性會列舉此產品實例的所有媒體磁片。 這個屬性會呼叫 MsiSourceListEnumMediaDisks。 以記錄物件的陣列形式傳回磁片資訊。
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: MediaDisks 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999148"
---
# <a name="productmediadisks-property"></a><span data-ttu-id="29077-105">MediaDisks 屬性</span><span class="sxs-lookup"><span data-stu-id="29077-105">Product.MediaDisks property</span></span>

<span data-ttu-id="29077-106">**MediaDisks** 屬性會列舉此產品實例的所有媒體磁片。</span><span class="sxs-lookup"><span data-stu-id="29077-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="29077-107">這個屬性會呼叫 [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)。</span><span class="sxs-lookup"><span data-stu-id="29077-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="29077-108">以 [**記錄**](record-object.md) 物件的陣列形式傳回磁片資訊。</span><span class="sxs-lookup"><span data-stu-id="29077-108">Returns the disk information as an array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="29077-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="29077-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="29077-110">語法</span><span class="sxs-lookup"><span data-stu-id="29077-110">Syntax</span></span>


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="29077-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="29077-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="29077-112">備註</span><span class="sxs-lookup"><span data-stu-id="29077-112">Remarks</span></span>

<span data-ttu-id="29077-113">在每一筆記錄中，第一個欄位包含磁片識別碼、第二個欄位包含磁片區標籤，而第三個欄位包含為磁片註冊的磁片提示。</span><span class="sxs-lookup"><span data-stu-id="29077-113">In each record, the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="29077-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="29077-114">Requirements</span></span>



| <span data-ttu-id="29077-115">需求</span><span class="sxs-lookup"><span data-stu-id="29077-115">Requirement</span></span> | <span data-ttu-id="29077-116">值</span><span class="sxs-lookup"><span data-stu-id="29077-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29077-117">版本</span><span class="sxs-lookup"><span data-stu-id="29077-117">Version</span></span><br/> | <span data-ttu-id="29077-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="29077-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="29077-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="29077-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="29077-120">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="29077-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="29077-121">DLL</span><span class="sxs-lookup"><span data-stu-id="29077-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="29077-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29077-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="29077-123">IID</span><span class="sxs-lookup"><span data-stu-id="29077-123">IID</span></span><br/>     | <span data-ttu-id="29077-124">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="29077-124">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="29077-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29077-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29077-126">**產品**</span><span class="sxs-lookup"><span data-stu-id="29077-126">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="29077-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="29077-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="29077-128">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="29077-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




