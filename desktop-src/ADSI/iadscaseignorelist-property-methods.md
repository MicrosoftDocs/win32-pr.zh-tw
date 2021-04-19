---
title: 'IADsCaseIgnoreList 屬性方法 (Iads .h) '
description: IADsCaseIgnoreList 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- IADsCaseIgnoreList 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984966"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="70fc1-105">IADsCaseIgnoreList 屬性方法</span><span class="sxs-lookup"><span data-stu-id="70fc1-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="70fc1-106">[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="70fc1-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="70fc1-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="70fc1-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="70fc1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="70fc1-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="70fc1-109">**CaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="70fc1-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="70fc1-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="70fc1-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="70fc1-111">不區分大小寫字串的排序次序。</span><span class="sxs-lookup"><span data-stu-id="70fc1-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="70fc1-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="70fc1-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="70fc1-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="70fc1-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="70fc1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="70fc1-114">Requirements</span></span>



| <span data-ttu-id="70fc1-115">需求</span><span class="sxs-lookup"><span data-stu-id="70fc1-115">Requirement</span></span> | <span data-ttu-id="70fc1-116">值</span><span class="sxs-lookup"><span data-stu-id="70fc1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70fc1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70fc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70fc1-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70fc1-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70fc1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70fc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70fc1-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70fc1-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70fc1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="70fc1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="70fc1-122"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="70fc1-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="70fc1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="70fc1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70fc1-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70fc1-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="70fc1-125">IID</span><span class="sxs-lookup"><span data-stu-id="70fc1-125">IID</span></span><br/>                      | <span data-ttu-id="70fc1-126">IID \_ IADsCaseIgnoreList 定義為7B66B533-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="70fc1-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="70fc1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70fc1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70fc1-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="70fc1-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="70fc1-129">**ADS \_ CASEIGNORE \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="70fc1-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





