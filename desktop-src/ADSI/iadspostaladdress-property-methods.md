---
title: 'IADsPostalAddress 屬性方法 (Iads .h) '
description: IADsPostalAddress 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- IADsPostalAddress 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968580"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="11c68-105">IADsPostalAddress 屬性方法</span><span class="sxs-lookup"><span data-stu-id="11c68-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="11c68-106">[**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="11c68-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="11c68-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="11c68-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="11c68-108">屬性</span><span class="sxs-lookup"><span data-stu-id="11c68-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="11c68-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="11c68-109">**PostalAddress**</span></span>
<span data-ttu-id="11c68-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="11c68-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="11c68-111">六個字串的陣列，其中包含使用者的郵遞區號位址。</span><span class="sxs-lookup"><span data-stu-id="11c68-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="11c68-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="11c68-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="11c68-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="11c68-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="11c68-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="11c68-114">Requirements</span></span>



| <span data-ttu-id="11c68-115">需求</span><span class="sxs-lookup"><span data-stu-id="11c68-115">Requirement</span></span> | <span data-ttu-id="11c68-116">值</span><span class="sxs-lookup"><span data-stu-id="11c68-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11c68-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11c68-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11c68-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11c68-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11c68-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11c68-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11c68-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11c68-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11c68-121">標頭</span><span class="sxs-lookup"><span data-stu-id="11c68-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c68-122"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="11c68-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="11c68-123">DLL</span><span class="sxs-lookup"><span data-stu-id="11c68-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c68-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c68-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="11c68-125">IID</span><span class="sxs-lookup"><span data-stu-id="11c68-125">IID</span></span><br/>                      | <span data-ttu-id="11c68-126">IID \_ IADsPostalAddress 定義為7ADECF29-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="11c68-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="11c68-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11c68-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c68-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="11c68-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="11c68-129">**ADS \_ POSTALADDRESS**</span><span class="sxs-lookup"><span data-stu-id="11c68-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





