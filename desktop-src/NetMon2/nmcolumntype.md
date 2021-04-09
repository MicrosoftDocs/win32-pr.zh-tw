---
description: 指定 NMCOLUMNVARIANT 結構的成員。
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: 'NMCOLUMNTYPE 列舉 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695391"
---
# <a name="nmcolumntype-enumeration"></a><span data-ttu-id="18f57-103">NMCOLUMNTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="18f57-103">NMCOLUMNTYPE enumeration</span></span>

<span data-ttu-id="18f57-104">**NMCOLUMNTYPE** 列舉會指定 [**NMCOLUMNVARIANT**](nmcolumnvariant.md)結構的成員。</span><span class="sxs-lookup"><span data-stu-id="18f57-104">The **NMCOLUMNTYPE** enumeration specifies the members of the [**NMCOLUMNVARIANT**](nmcolumnvariant.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18f57-105">Syntax</span></span>


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a><span data-ttu-id="18f57-106">常數</span><span class="sxs-lookup"><span data-stu-id="18f57-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="18f57-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE \_ UINT8**</span><span class="sxs-lookup"><span data-stu-id="18f57-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE\_UINT8**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-108">8位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="18f57-108">8-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE \_ SINT8**</span><span class="sxs-lookup"><span data-stu-id="18f57-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE\_SINT8**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-110">8位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="18f57-110">8-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UINT16**</span><span class="sxs-lookup"><span data-stu-id="18f57-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE\_UINT16**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-112">16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="18f57-112">16-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE \_ SINT16**</span><span class="sxs-lookup"><span data-stu-id="18f57-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE\_SINT16**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-114">16位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="18f57-114">16-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE \_ UINT32**</span><span class="sxs-lookup"><span data-stu-id="18f57-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE\_UINT32**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-116">32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="18f57-116">32-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="18f57-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE\_SINT32**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-118">32 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="18f57-118">32-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE \_ FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="18f57-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE\_FLOAT64**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-120">64位浮點數。</span><span class="sxs-lookup"><span data-stu-id="18f57-120">64-bit float.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="18f57-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE\_FRAME**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-122">畫面格編號。</span><span class="sxs-lookup"><span data-stu-id="18f57-122">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE \_ YESNO**</span><span class="sxs-lookup"><span data-stu-id="18f57-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE\_YESNO**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-124">「是」或「否」。</span><span class="sxs-lookup"><span data-stu-id="18f57-124">"Yes" or "No".</span></span>

</dd> <dt>

<span data-ttu-id="18f57-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE \_ ONOFF**</span><span class="sxs-lookup"><span data-stu-id="18f57-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE\_ONOFF**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-126">「開啟」或「關閉」</span><span class="sxs-lookup"><span data-stu-id="18f57-126">"On" or "Off"</span></span>

</dd> <dt>

<span data-ttu-id="18f57-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE \_ TRUEFALSE**</span><span class="sxs-lookup"><span data-stu-id="18f57-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE\_TRUEFALSE**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-128">"True" 或 "False"。</span><span class="sxs-lookup"><span data-stu-id="18f57-128">"True" or "False".</span></span>

</dd> <dt>

<span data-ttu-id="18f57-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE \_ MACADDR**</span><span class="sxs-lookup"><span data-stu-id="18f57-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE\_MACADDR**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-130">MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="18f57-130">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE \_ IPXADDR**</span><span class="sxs-lookup"><span data-stu-id="18f57-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE\_IPXADDR**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-132">IPX 位址。</span><span class="sxs-lookup"><span data-stu-id="18f57-132">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE \_ IPADDR**</span><span class="sxs-lookup"><span data-stu-id="18f57-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE\_IPADDR**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-134">IP 位址。</span><span class="sxs-lookup"><span data-stu-id="18f57-134">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE \_ VARTIME**</span><span class="sxs-lookup"><span data-stu-id="18f57-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE\_VARTIME**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-136">變異時間。</span><span class="sxs-lookup"><span data-stu-id="18f57-136">Variant time.</span></span>

</dd> <dt>

<span data-ttu-id="18f57-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="18f57-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="18f57-138">字串的指標。</span><span class="sxs-lookup"><span data-stu-id="18f57-138">Pointer to a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18f57-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="18f57-139">Requirements</span></span>



| <span data-ttu-id="18f57-140">需求</span><span class="sxs-lookup"><span data-stu-id="18f57-140">Requirement</span></span> | <span data-ttu-id="18f57-141">值</span><span class="sxs-lookup"><span data-stu-id="18f57-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="18f57-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18f57-142">Minimum supported client</span></span><br/> | <span data-ttu-id="18f57-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18f57-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="18f57-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18f57-144">Minimum supported server</span></span><br/> | <span data-ttu-id="18f57-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18f57-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="18f57-146">標頭</span><span class="sxs-lookup"><span data-stu-id="18f57-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f57-147"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="18f57-147"><dt>Netmon.h</dt></span></span> </dl> |



 

 




