---
title: 'IADsHold 屬性方法 (Iads .h) '
description: IADsHold 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- IADsHold 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105137"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="b98ec-105">IADsHold 屬性方法</span><span class="sxs-lookup"><span data-stu-id="b98ec-105">IADsHold Property Methods</span></span>

<span data-ttu-id="b98ec-106">[**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="b98ec-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="b98ec-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="b98ec-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b98ec-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b98ec-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b98ec-109">**金額**</span><span class="sxs-lookup"><span data-stu-id="b98ec-109">**Amount**</span></span>
<span data-ttu-id="b98ec-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b98ec-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b98ec-111">當伺服器檢查使用者的帳戶餘額時，對使用者收取的費用。</span><span class="sxs-lookup"><span data-stu-id="b98ec-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="b98ec-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b98ec-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b98ec-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="b98ec-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b98ec-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="b98ec-114">**ObjectName**</span></span>
<span data-ttu-id="b98ec-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b98ec-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b98ec-116">代表持有使用者的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="b98ec-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="b98ec-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b98ec-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b98ec-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b98ec-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="b98ec-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b98ec-119">Requirements</span></span>



| <span data-ttu-id="b98ec-120">需求</span><span class="sxs-lookup"><span data-stu-id="b98ec-120">Requirement</span></span> | <span data-ttu-id="b98ec-121">值</span><span class="sxs-lookup"><span data-stu-id="b98ec-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b98ec-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b98ec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b98ec-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b98ec-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b98ec-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b98ec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b98ec-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b98ec-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b98ec-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b98ec-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b98ec-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="b98ec-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b98ec-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b98ec-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b98ec-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b98ec-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b98ec-130">IID</span><span class="sxs-lookup"><span data-stu-id="b98ec-130">IID</span></span><br/>                      | <span data-ttu-id="b98ec-131">IID \_ IADsHold 定義為 B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="b98ec-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b98ec-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b98ec-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b98ec-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="b98ec-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





