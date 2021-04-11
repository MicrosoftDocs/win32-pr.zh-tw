---
title: 'IADsOctetList 屬性方法 (Iads .h) '
description: IADsOctetList 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- IADsOctetList 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934814"
---
# <a name="iadsoctetlist-property-methods"></a><span data-ttu-id="0c6ba-105">IADsOctetList 屬性方法</span><span class="sxs-lookup"><span data-stu-id="0c6ba-105">IADsOctetList Property Methods</span></span>

<span data-ttu-id="0c6ba-106">[**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c6ba-106">The property method of the [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) interface sets the property described in the following table.</span></span> <span data-ttu-id="0c6ba-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="0c6ba-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0c6ba-108">屬性</span><span class="sxs-lookup"><span data-stu-id="0c6ba-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0c6ba-109">**OctetList**</span><span class="sxs-lookup"><span data-stu-id="0c6ba-109">**OctetList**</span></span>
<span data-ttu-id="0c6ba-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c6ba-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c6ba-111">位元組陣列的排序序列。</span><span class="sxs-lookup"><span data-stu-id="0c6ba-111">An ordered sequence of byte arrays.</span></span>

<dt>

<span data-ttu-id="0c6ba-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0c6ba-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c6ba-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="0c6ba-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="0c6ba-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c6ba-114">Requirements</span></span>



| <span data-ttu-id="0c6ba-115">需求</span><span class="sxs-lookup"><span data-stu-id="0c6ba-115">Requirement</span></span> | <span data-ttu-id="0c6ba-116">值</span><span class="sxs-lookup"><span data-stu-id="0c6ba-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6ba-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c6ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c6ba-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c6ba-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c6ba-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c6ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c6ba-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c6ba-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c6ba-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0c6ba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c6ba-122"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c6ba-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0c6ba-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0c6ba-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c6ba-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c6ba-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c6ba-125">IID</span><span class="sxs-lookup"><span data-stu-id="0c6ba-125">IID</span></span><br/>                      | <span data-ttu-id="0c6ba-126">IID \_ IADsOctetList 定義為7B28B80F-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="0c6ba-126">IID\_IADsOctetList is defined as 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="0c6ba-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c6ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6ba-128">**IADsOctetList**</span><span class="sxs-lookup"><span data-stu-id="0c6ba-128">**IADsOctetList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[<span data-ttu-id="0c6ba-129">**ADS \_ 八位 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="0c6ba-129">**ADS\_OCTET\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





