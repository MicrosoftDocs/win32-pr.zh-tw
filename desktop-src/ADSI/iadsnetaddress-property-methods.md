---
title: 'IADsNetAddress 屬性方法 (Iads .h) '
description: IADsNetAddress 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- IADsNetAddress 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686205"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="425c1-105">IADsNetAddress 屬性方法</span><span class="sxs-lookup"><span data-stu-id="425c1-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="425c1-106">[**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="425c1-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="425c1-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="425c1-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="425c1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="425c1-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="425c1-109">**位址**</span><span class="sxs-lookup"><span data-stu-id="425c1-109">**Address**</span></span>
<span data-ttu-id="425c1-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="425c1-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="425c1-111">網路位址。</span><span class="sxs-lookup"><span data-stu-id="425c1-111">A network address.</span></span>

<dt>

<span data-ttu-id="425c1-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="425c1-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="425c1-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="425c1-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="425c1-114">**AddressType**</span><span class="sxs-lookup"><span data-stu-id="425c1-114">**AddressType**</span></span>
<span data-ttu-id="425c1-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="425c1-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="425c1-116">通訊協定的類型。</span><span class="sxs-lookup"><span data-stu-id="425c1-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="425c1-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="425c1-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="425c1-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="425c1-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="425c1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="425c1-119">Requirements</span></span>



| <span data-ttu-id="425c1-120">需求</span><span class="sxs-lookup"><span data-stu-id="425c1-120">Requirement</span></span> | <span data-ttu-id="425c1-121">值</span><span class="sxs-lookup"><span data-stu-id="425c1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="425c1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="425c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="425c1-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="425c1-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="425c1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="425c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="425c1-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="425c1-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="425c1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="425c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="425c1-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="425c1-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="425c1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="425c1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="425c1-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="425c1-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="425c1-130">IID</span><span class="sxs-lookup"><span data-stu-id="425c1-130">IID</span></span><br/>                      | <span data-ttu-id="425c1-131">IID \_ IADsNetAddress 定義為 B21A50A9-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="425c1-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="425c1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="425c1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425c1-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="425c1-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="425c1-134">**ADS \_ NETADDRESS**</span><span class="sxs-lookup"><span data-stu-id="425c1-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





