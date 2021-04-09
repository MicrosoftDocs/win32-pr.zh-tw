---
title: 'ADSI 單一資料型別 (Iads .h) '
description: ADSI)  (Active Directory 服務介面會定義和使用下列簡單的資料類型。
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024734"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="5ba6d-114">ADSI 單一資料型別</span><span class="sxs-lookup"><span data-stu-id="5ba6d-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="5ba6d-115">ADSI)  (Active Directory 服務介面會定義和使用下列簡單的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5ba6d-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="5ba6d-116">**ADS \_ 布林值**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ba6d-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-118">**ADS \_ 案例 \_ 精確 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-120">**廣告 \_ 案例 \_ 忽略 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-122">**ADS \_ DN \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-124">**ADS \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ba6d-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-126">**ADS \_ 大型 \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="5ba6d-127">**大型 \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="5ba6d-128">**ADS \_ 數值 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-130">**ADS \_ 物件 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-132">**ADS \_ 可列印 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-134">**ADS \_ 搜尋 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5ba6d-135">HANDLE</span><span class="sxs-lookup"><span data-stu-id="5ba6d-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="5ba6d-136">**ADS \_ UTC \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="5ba6d-137">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="5ba6d-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ba6d-138">備註</span><span class="sxs-lookup"><span data-stu-id="5ba6d-138">Remarks</span></span>

<span data-ttu-id="5ba6d-139">當 ADSI 讀取已定義為 LDAP 架構中之 **整數** 的屬性時，它一律會將整數處理為32位值，而且可能會截斷資料。</span><span class="sxs-lookup"><span data-stu-id="5ba6d-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="5ba6d-140">這只是允許任意大小的整數值之 LDAP 伺服器的考慮。</span><span class="sxs-lookup"><span data-stu-id="5ba6d-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="5ba6d-141">如果屬性是延伸架構所定義的自訂屬性，則可將自訂屬性定義為字串來避免此問題。</span><span class="sxs-lookup"><span data-stu-id="5ba6d-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ba6d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ba6d-142">Requirements</span></span>



| <span data-ttu-id="5ba6d-143">需求</span><span class="sxs-lookup"><span data-stu-id="5ba6d-143">Requirement</span></span> | <span data-ttu-id="5ba6d-144">值</span><span class="sxs-lookup"><span data-stu-id="5ba6d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5ba6d-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ba6d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5ba6d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ba6d-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="5ba6d-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ba6d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5ba6d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ba6d-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="5ba6d-149">標頭</span><span class="sxs-lookup"><span data-stu-id="5ba6d-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ba6d-150"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba6d-150"><dt>Iads.h</dt></span></span> </dl> |



 

