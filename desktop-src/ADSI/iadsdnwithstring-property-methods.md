---
title: 'IADsDNWithString 屬性方法 (Iads .h) '
description: IADsDNWithString 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- IADsDNWithString 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969608"
---
# <a name="iadsdnwithstring-property-methods"></a><span data-ttu-id="42380-105">IADsDNWithString 屬性方法</span><span class="sxs-lookup"><span data-stu-id="42380-105">IADsDNWithString Property Methods</span></span>

<span data-ttu-id="42380-106">[**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="42380-106">The property method of the [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) interface sets the property described in the following table.</span></span> <span data-ttu-id="42380-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="42380-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="42380-108">屬性</span><span class="sxs-lookup"><span data-stu-id="42380-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="42380-109">**DNString**</span><span class="sxs-lookup"><span data-stu-id="42380-109">**DNString**</span></span>
<span data-ttu-id="42380-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="42380-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="42380-111">與字串值相關聯的 DN 字串。</span><span class="sxs-lookup"><span data-stu-id="42380-111">The DN string associated with a string value.</span></span>

<dt>

<span data-ttu-id="42380-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="42380-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42380-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="42380-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="42380-114">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="42380-114">**StringValue**</span></span>
<span data-ttu-id="42380-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="42380-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="42380-116">與物件之 DN 相關聯的字串值。</span><span class="sxs-lookup"><span data-stu-id="42380-116">The string value associated with a DN of an object.</span></span>

<dt>

<span data-ttu-id="42380-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="42380-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42380-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="42380-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="42380-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="42380-119">Requirements</span></span>



| <span data-ttu-id="42380-120">需求</span><span class="sxs-lookup"><span data-stu-id="42380-120">Requirement</span></span> | <span data-ttu-id="42380-121">值</span><span class="sxs-lookup"><span data-stu-id="42380-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42380-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42380-122">Minimum supported client</span></span><br/> | <span data-ttu-id="42380-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42380-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42380-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42380-124">Minimum supported server</span></span><br/> | <span data-ttu-id="42380-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42380-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42380-126">標頭</span><span class="sxs-lookup"><span data-stu-id="42380-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="42380-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="42380-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="42380-128">DLL</span><span class="sxs-lookup"><span data-stu-id="42380-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42380-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42380-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="42380-130">IID</span><span class="sxs-lookup"><span data-stu-id="42380-130">IID</span></span><br/>                      | <span data-ttu-id="42380-131">IID \_ IADsDNWithString 定義為370DF02E-F934-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="42380-131">IID\_IADsDNWithString is defined as 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="42380-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42380-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42380-133">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="42380-133">**IADsDNWithString**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[<span data-ttu-id="42380-134">**\_ \_ 具有字串的 ADS DN \_**</span><span class="sxs-lookup"><span data-stu-id="42380-134">**ADS\_DN\_WITH\_STRING**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





