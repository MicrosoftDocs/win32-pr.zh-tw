---
title: 'IADsFaxNumber 屬性方法 (Iads .h) '
description: IADsFaxNumber 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- IADsFaxNumber 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966333"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="49fed-105">IADsFaxNumber 屬性方法</span><span class="sxs-lookup"><span data-stu-id="49fed-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="49fed-106">[**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="49fed-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="49fed-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="49fed-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="49fed-108">屬性</span><span class="sxs-lookup"><span data-stu-id="49fed-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="49fed-109">**參數**</span><span class="sxs-lookup"><span data-stu-id="49fed-109">**Parameters**</span></span>
<span data-ttu-id="49fed-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49fed-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="49fed-111">傳真電腦的參數。</span><span class="sxs-lookup"><span data-stu-id="49fed-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="49fed-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49fed-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="49fed-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="49fed-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="49fed-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="49fed-114">**TelephoneNumber**</span></span>
<span data-ttu-id="49fed-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49fed-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="49fed-116">傳真電腦的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="49fed-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="49fed-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49fed-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="49fed-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="49fed-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="49fed-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="49fed-119">Requirements</span></span>



| <span data-ttu-id="49fed-120">需求</span><span class="sxs-lookup"><span data-stu-id="49fed-120">Requirement</span></span> | <span data-ttu-id="49fed-121">值</span><span class="sxs-lookup"><span data-stu-id="49fed-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49fed-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49fed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49fed-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49fed-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49fed-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49fed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49fed-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49fed-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49fed-126">標頭</span><span class="sxs-lookup"><span data-stu-id="49fed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="49fed-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="49fed-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="49fed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="49fed-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49fed-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49fed-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="49fed-130">IID</span><span class="sxs-lookup"><span data-stu-id="49fed-130">IID</span></span><br/>                      | <span data-ttu-id="49fed-131">IID \_ IADsFaxNumber 定義為 A910DEA9-4680-11D1-0A3B-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="49fed-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="49fed-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49fed-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fed-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="49fed-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="49fed-134">**ADS \_ FAXNUMBER**</span><span class="sxs-lookup"><span data-stu-id="49fed-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





