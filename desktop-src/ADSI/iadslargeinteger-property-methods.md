---
title: 'IADsLargeInteger 屬性方法 (Iads .h) '
description: IADsLargeInteger 介面的屬性方法會取得並設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- IADsLargeInteger 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984965"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="e59fb-105">IADsLargeInteger 屬性方法</span><span class="sxs-lookup"><span data-stu-id="e59fb-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="e59fb-106">[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)介面的屬性方法會取得並設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="e59fb-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="e59fb-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="e59fb-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e59fb-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e59fb-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="e59fb-109">**HighPart**</span><span class="sxs-lookup"><span data-stu-id="e59fb-109">**HighPart**</span></span>
<span data-ttu-id="e59fb-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e59fb-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="e59fb-111">整數的高部分。</span><span class="sxs-lookup"><span data-stu-id="e59fb-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="e59fb-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e59fb-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e59fb-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="e59fb-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e59fb-114">**LowPart**</span><span class="sxs-lookup"><span data-stu-id="e59fb-114">**LowPart**</span></span>
<span data-ttu-id="e59fb-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e59fb-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="e59fb-116">整數的低部分。</span><span class="sxs-lookup"><span data-stu-id="e59fb-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="e59fb-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e59fb-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e59fb-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="e59fb-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="e59fb-119">備註</span><span class="sxs-lookup"><span data-stu-id="e59fb-119">Remarks</span></span>

<span data-ttu-id="e59fb-120">如果 largeInt 是 **LargeInteger** 類型，則會根據下列公式，為 **HighPart** 和 **LowPart** 的值指定其值。</span><span class="sxs-lookup"><span data-stu-id="e59fb-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="e59fb-121">範例</span><span class="sxs-lookup"><span data-stu-id="e59fb-121">Examples</span></span>

<span data-ttu-id="e59fb-122">下列 Visual Basic 程式碼範例會將大型整數設定為43937327281。</span><span class="sxs-lookup"><span data-stu-id="e59fb-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="e59fb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e59fb-123">Requirements</span></span>



| <span data-ttu-id="e59fb-124">需求</span><span class="sxs-lookup"><span data-stu-id="e59fb-124">Requirement</span></span> | <span data-ttu-id="e59fb-125">值</span><span class="sxs-lookup"><span data-stu-id="e59fb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e59fb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e59fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e59fb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e59fb-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e59fb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e59fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e59fb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e59fb-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e59fb-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e59fb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e59fb-131"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="e59fb-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="e59fb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e59fb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e59fb-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e59fb-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="e59fb-134">IID</span><span class="sxs-lookup"><span data-stu-id="e59fb-134">IID</span></span><br/>                      | <span data-ttu-id="e59fb-135">IID \_ IADsLargeInteger 定義為9068270B-0939-11D1-8BE1-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="e59fb-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="e59fb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e59fb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59fb-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="e59fb-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





