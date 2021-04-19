---
title: 'IADsTypedName 屬性方法 (Iads .h) '
description: IADsTypedName 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- IADsTypedName 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991124"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="160d2-105">IADsTypedName 屬性方法</span><span class="sxs-lookup"><span data-stu-id="160d2-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="160d2-106">[**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="160d2-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="160d2-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="160d2-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="160d2-108">屬性</span><span class="sxs-lookup"><span data-stu-id="160d2-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="160d2-109">**間隔**</span><span class="sxs-lookup"><span data-stu-id="160d2-109">**Interval**</span></span>
<span data-ttu-id="160d2-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="160d2-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="160d2-111">物件參考的頻率。</span><span class="sxs-lookup"><span data-stu-id="160d2-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="160d2-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="160d2-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="160d2-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="160d2-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="160d2-114">**Level**</span><span class="sxs-lookup"><span data-stu-id="160d2-114">**Level**</span></span>
<span data-ttu-id="160d2-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="160d2-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="160d2-116">與物件相關聯的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="160d2-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="160d2-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="160d2-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="160d2-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="160d2-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="160d2-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="160d2-119">**ObjectName**</span></span>
<span data-ttu-id="160d2-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="160d2-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="160d2-121">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="160d2-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="160d2-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="160d2-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="160d2-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="160d2-123">Scripting data type: **BSTR**</span></span>
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

 

## <a name="requirements"></a><span data-ttu-id="160d2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="160d2-124">Requirements</span></span>



| <span data-ttu-id="160d2-125">需求</span><span class="sxs-lookup"><span data-stu-id="160d2-125">Requirement</span></span> | <span data-ttu-id="160d2-126">值</span><span class="sxs-lookup"><span data-stu-id="160d2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="160d2-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="160d2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="160d2-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="160d2-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="160d2-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="160d2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="160d2-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="160d2-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="160d2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="160d2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="160d2-132"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="160d2-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="160d2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="160d2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="160d2-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="160d2-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="160d2-135">IID</span><span class="sxs-lookup"><span data-stu-id="160d2-135">IID</span></span><br/>                      | <span data-ttu-id="160d2-136">IID \_ IADsTypedName 定義為 B371A349-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="160d2-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="160d2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="160d2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="160d2-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="160d2-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="160d2-139">**ADS \_ TYPEDNAME**</span><span class="sxs-lookup"><span data-stu-id="160d2-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





