---
title: 'IADsDNWithBinary 屬性方法 (Iads .h) '
description: IADsDNWithBinary 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- IADsDNWithBinary 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105149"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="16aaf-105">IADsDNWithBinary 屬性方法</span><span class="sxs-lookup"><span data-stu-id="16aaf-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="16aaf-106">[**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="16aaf-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="16aaf-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="16aaf-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="16aaf-108">屬性</span><span class="sxs-lookup"><span data-stu-id="16aaf-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="16aaf-109">**BinaryValue**</span><span class="sxs-lookup"><span data-stu-id="16aaf-109">**BinaryValue**</span></span>
<span data-ttu-id="16aaf-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="16aaf-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="16aaf-111">與 DN 相關聯之物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="16aaf-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="16aaf-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="16aaf-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="16aaf-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="16aaf-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="16aaf-114">**DNString**</span><span class="sxs-lookup"><span data-stu-id="16aaf-114">**DNString**</span></span>
<span data-ttu-id="16aaf-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="16aaf-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="16aaf-116">與物件之 GUID 相關聯的 DN 字串。</span><span class="sxs-lookup"><span data-stu-id="16aaf-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="16aaf-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="16aaf-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="16aaf-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="16aaf-118">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="16aaf-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="16aaf-119">Requirements</span></span>



| <span data-ttu-id="16aaf-120">需求</span><span class="sxs-lookup"><span data-stu-id="16aaf-120">Requirement</span></span> | <span data-ttu-id="16aaf-121">值</span><span class="sxs-lookup"><span data-stu-id="16aaf-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16aaf-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16aaf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16aaf-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16aaf-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16aaf-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16aaf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16aaf-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16aaf-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16aaf-126">標頭</span><span class="sxs-lookup"><span data-stu-id="16aaf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="16aaf-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="16aaf-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="16aaf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="16aaf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16aaf-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16aaf-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="16aaf-130">IID</span><span class="sxs-lookup"><span data-stu-id="16aaf-130">IID</span></span><br/>                      | <span data-ttu-id="16aaf-131">IID \_ IADsDNWithBinary 定義為7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="16aaf-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="16aaf-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16aaf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16aaf-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="16aaf-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="16aaf-134">**\_ \_ 使用二進位的 ADS DN \_**</span><span class="sxs-lookup"><span data-stu-id="16aaf-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





