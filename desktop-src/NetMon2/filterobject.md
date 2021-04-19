---
description: 定義顯示篩選準則的單一物件。
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: 'FILTEROBJECT 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986302"
---
# <a name="filterobject-structure"></a><span data-ttu-id="a0f48-103">FILTEROBJECT 結構</span><span class="sxs-lookup"><span data-stu-id="a0f48-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="a0f48-104">**FILTEROBJECT** 結構會定義顯示篩選的單一物件。</span><span class="sxs-lookup"><span data-stu-id="a0f48-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="a0f48-105">[**FilterAddObject**](filteraddobject.md)函數會使用 **FILTEROBJECT** 來建立顯示篩選。</span><span class="sxs-lookup"><span data-stu-id="a0f48-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f48-106">語法</span><span class="sxs-lookup"><span data-stu-id="a0f48-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="a0f48-107">成員</span><span class="sxs-lookup"><span data-stu-id="a0f48-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0f48-108">**動作**</span><span class="sxs-lookup"><span data-stu-id="a0f48-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-109">指定 **FILTEROBJECT** 動作的旗標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="a0f48-110">旗標可以指定屬性、值或運算子。</span><span class="sxs-lookup"><span data-stu-id="a0f48-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="a0f48-111">下表列出動作成員屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="a0f48-112">值</span><span class="sxs-lookup"><span data-stu-id="a0f48-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="a0f48-113">意義</span><span class="sxs-lookup"><span data-stu-id="a0f48-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="a0f48-114"><dt>**FILTERACTION \_ 屬性**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="a0f48-115">包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a0f48-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="a0f48-116"><dt>**FILTERACTION \_ PROPERTYEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="a0f48-117">表示已定義篩選動作屬性。</span><span class="sxs-lookup"><span data-stu-id="a0f48-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="a0f48-118">下表列出動作成員值旗標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="a0f48-119">值</span><span class="sxs-lookup"><span data-stu-id="a0f48-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="a0f48-120">意義</span><span class="sxs-lookup"><span data-stu-id="a0f48-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="a0f48-121"><dt>**FILTERACTION \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="a0f48-122">包含這個值。</span><span class="sxs-lookup"><span data-stu-id="a0f48-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="a0f48-123"><dt>**FILTERACTION \_ 字串**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="a0f48-124">包含這個字串。</span><span class="sxs-lookup"><span data-stu-id="a0f48-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="a0f48-125"><dt>**FILTERACTION \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="a0f48-126">包含此陣列。</span><span class="sxs-lookup"><span data-stu-id="a0f48-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="a0f48-127"><dt>**FILTERACTION \_ CONTAINSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="a0f48-128">指出屬性包含不區分大小寫的子字串。</span><span class="sxs-lookup"><span data-stu-id="a0f48-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="a0f48-129"><dt>**FILTERACTION \_ CONTAINS**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="a0f48-130">指出屬性包含區分大小寫的子字串。</span><span class="sxs-lookup"><span data-stu-id="a0f48-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="a0f48-131"><dt>**FILTERACTION \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="a0f48-132">包含 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="a0f48-133"><dt>**FILTERACTION \_ ADDRESSANY**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="a0f48-134">符合任何 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="a0f48-135"><dt>**FILTERACTION \_ 來源**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="a0f48-136">表示 **從 MAC** 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="a0f48-137"><dt>**FILTERACTION \_ 至**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="a0f48-138">表示 **至 MAC** 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="a0f48-139"><dt>**FILTERACTION \_ FROMTO**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="a0f48-140">表示與 MAC 位址的 **之間** 的配對。</span><span class="sxs-lookup"><span data-stu-id="a0f48-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="a0f48-141"><dt>**FILTERACTION \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="a0f48-142">包含大整數。</span><span class="sxs-lookup"><span data-stu-id="a0f48-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="a0f48-143"><dt>**FILTERACTION \_ TIME**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="a0f48-144">包含 **SYSTEMTIME** 結構。</span><span class="sxs-lookup"><span data-stu-id="a0f48-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="a0f48-145"><dt>**FILTERACTION \_ ADDR \_ 乙太幣**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="a0f48-146">包含乙太網路 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="a0f48-147"><dt>**FILTERACTION \_ 位址 \_ 權杖**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="a0f48-148">包含權杖環形 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="a0f48-149"><dt>**FILTERACTION \_ ADDR 的 \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="a0f48-150">包含 FDDI MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="a0f48-151"><dt>**FILTERACTION \_ 位址 \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="a0f48-152">包含 IPX MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="a0f48-153"><dt>**FILTERACTION \_ 位址 \_ IP**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="a0f48-154">包含 IP MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="a0f48-155"><dt>**FILTERACTION \_ OID**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="a0f48-156">包含 (OID) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0f48-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="a0f48-157">下表列出動作成員運算子旗標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="a0f48-158">值</span><span class="sxs-lookup"><span data-stu-id="a0f48-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="a0f48-159">意義</span><span class="sxs-lookup"><span data-stu-id="a0f48-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="a0f48-160"><dt>**FILTERACTION \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="a0f48-161">指出不正確篩選動作。</span><span class="sxs-lookup"><span data-stu-id="a0f48-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="a0f48-162"><dt>**FILTERACTION \_ 和**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="a0f48-163">表示邏輯 **AND** 語句。</span><span class="sxs-lookup"><span data-stu-id="a0f48-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="a0f48-164"><dt>**FILTERACTION \_ 或**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="a0f48-165">表示邏輯 **OR** 語句。</span><span class="sxs-lookup"><span data-stu-id="a0f48-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="a0f48-166"><dt>**FILTERACTION \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="a0f48-167">表示邏輯互斥 **OR** (XOR) 語句。</span><span class="sxs-lookup"><span data-stu-id="a0f48-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="a0f48-168"><dt>**FILTERACTION \_ NOT**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="a0f48-169">表示邏輯 **NOT** 語句。</span><span class="sxs-lookup"><span data-stu-id="a0f48-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="a0f48-170"><dt>**FILTERACTION \_ EQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="a0f48-171">篩選動作相等且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="a0f48-172"><dt>**FILTERACTION \_ 相等**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="a0f48-173">篩選動作相等且區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="a0f48-174"><dt>**FILTERACTION \_ NOTEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="a0f48-175">邏輯 **NOT** 語句相等且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="a0f48-176"><dt>**FILTERACTION \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="a0f48-177">邏輯 **NOT** 語句相等，而且區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="a0f48-178"><dt>**FILTERACTION \_ GREATERNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="a0f48-179">篩選動作大於 (>) ，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="a0f48-180"><dt>**FILTERACTION \_ 更多**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="a0f48-181">篩選動作大於 (>) 和區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="a0f48-182"><dt>**FILTERACTION \_ LESSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="a0f48-183">篩選動作小於 (<) ，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="a0f48-184"><dt>**\_LESS 篩選**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="a0f48-185">篩選動作小於 (<) 和區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="a0f48-186"><dt>**FILTERACTION \_ GREATEREQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="a0f48-187">篩選動作大於或等於 (>=) 且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="a0f48-188"><dt>**FILTERACTION \_ GREATEREQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="a0f48-189">篩選動作大於或等於 (>=) 和區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="a0f48-190"><dt>**FILTERACTION \_ LESSEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="a0f48-191">篩選動作小於或等於 (<=) 且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="a0f48-192"><dt>**FILTERACTION \_ LESSEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="a0f48-193">篩選動作小於或等於 (<=) ，而且會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0f48-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="a0f48-194"><dt>**FILTERACTION \_ PLUS**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="a0f48-195">將運算子新增 (+) 。</span><span class="sxs-lookup"><span data-stu-id="a0f48-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="a0f48-196"><dt>**FILTERACTION \_ 減號**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="a0f48-197">減去運算子 (-) 。</span><span class="sxs-lookup"><span data-stu-id="a0f48-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="a0f48-198"><dt>**FILTERACTION \_ AREBITSON**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="a0f48-199">表示位運算。</span><span class="sxs-lookup"><span data-stu-id="a0f48-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="a0f48-200"><dt>**FILTERACTION \_ AREBITSOFF**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="a0f48-201">表示非位運算。</span><span class="sxs-lookup"><span data-stu-id="a0f48-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="a0f48-202"><dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="a0f48-203">表示選取的通訊協定存在。</span><span class="sxs-lookup"><span data-stu-id="a0f48-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="a0f48-204"><dt>**FILTERACTION \_ PROTOCOLEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="a0f48-205">表示選取的通訊協定存在。</span><span class="sxs-lookup"><span data-stu-id="a0f48-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="a0f48-206"><dt>**FILTERACTION \_ ARRAYEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="a0f48-207">指出陣列內容相等。</span><span class="sxs-lookup"><span data-stu-id="a0f48-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="a0f48-208">旗標必須與 **FILTERACTION \_ 陣列** 結構一起使用。</span><span class="sxs-lookup"><span data-stu-id="a0f48-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="a0f48-209"><dt>**FILTERACTION \_ DEREFPROPERTY**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="a0f48-210">描述從通訊協定到位移 (位元組) 的模式比對。</span><span class="sxs-lookup"><span data-stu-id="a0f48-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="a0f48-211"><dt>**FILTERACTION \_ OID \_ CONTAINS**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="a0f48-212">評估物件識別碼內的子字串。</span><span class="sxs-lookup"><span data-stu-id="a0f48-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="a0f48-213">動作必須與 **FILTERACTION \_ OID** 結構一起使用。</span><span class="sxs-lookup"><span data-stu-id="a0f48-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="a0f48-214"><dt>**FILTERACTION \_ OID \_ 開頭 \_ 為**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="a0f48-215">評估開始物件識別碼的子字串。</span><span class="sxs-lookup"><span data-stu-id="a0f48-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="a0f48-216">旗標必須與 **FILTERACTION \_ OID** 一起使用。</span><span class="sxs-lookup"><span data-stu-id="a0f48-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="a0f48-217"><dt>**FILTERACTION \_ OID \_ 結尾 \_ 為**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="a0f48-218">評估結束物件識別碼的子字串。</span><span class="sxs-lookup"><span data-stu-id="a0f48-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="a0f48-219">旗標必須與 **FILTERACTION \_ OID** 一起使用。</span><span class="sxs-lookup"><span data-stu-id="a0f48-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="a0f48-220"><dt>**FILTERACTION \_ ADDR \_ VINES**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="a0f48-221">包含 Vines MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a0f48-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="a0f48-222"><dt>**FILTERACTION \_ 運算式**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="a0f48-223">包含動作運算式。</span><span class="sxs-lookup"><span data-stu-id="a0f48-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="a0f48-224"><dt>**FILTERACTION \_ BOOL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="a0f48-225">包含 **BOOL** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a0f48-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="a0f48-226"><dt>**\_ \_ 接下來的篩選方向**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="a0f48-227">控制在捕捉檔案內 (下一個框架) 的順序方向。</span><span class="sxs-lookup"><span data-stu-id="a0f48-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="a0f48-228"><dt>**\_前篩選方向 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="a0f48-229">控制在捕獲檔案內 (上一個框架) 的順序方向。</span><span class="sxs-lookup"><span data-stu-id="a0f48-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="a0f48-230">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="a0f48-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-231">屬性索引鍵的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a0f48-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-232">**值**</span><span class="sxs-lookup"><span data-stu-id="a0f48-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-233">物件的值。</span><span class="sxs-lookup"><span data-stu-id="a0f48-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-234">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="a0f48-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-235">顯示篩選器通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a0f48-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="a0f48-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-237">陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-238">**lpProtocolTable**</span><span class="sxs-lookup"><span data-stu-id="a0f48-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-239">通訊協定清單的指標，其設計目的是要測試框架中的通訊協定是否存在。</span><span class="sxs-lookup"><span data-stu-id="a0f48-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-240">**lpAddress**</span><span class="sxs-lookup"><span data-stu-id="a0f48-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-241">核心類型位址的指標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="a0f48-242">例如，MAC 或 IP。</span><span class="sxs-lookup"><span data-stu-id="a0f48-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-243">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="a0f48-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-244">Windows NT 或 Windows 2000 應用程式中使用的雙 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="a0f48-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-245">**lpTime**</span><span class="sxs-lookup"><span data-stu-id="a0f48-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-246">**SYSTEMTIME** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a0f48-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-247">**lpOID**</span><span class="sxs-lookup"><span data-stu-id="a0f48-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-248">**物件 \_ 識別碼** 的指標， (OID) 結構。</span><span class="sxs-lookup"><span data-stu-id="a0f48-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="a0f48-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-250">框架中的數位（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0f48-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-251">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="a0f48-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-252">用來比較陣列的 FILTEROBJECT 結構的位移位元組值。</span><span class="sxs-lookup"><span data-stu-id="a0f48-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="a0f48-253">**pNext**</span><span class="sxs-lookup"><span data-stu-id="a0f48-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="a0f48-254">保留的。</span><span class="sxs-lookup"><span data-stu-id="a0f48-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0f48-255">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0f48-255">Requirements</span></span>



| <span data-ttu-id="a0f48-256">需求</span><span class="sxs-lookup"><span data-stu-id="a0f48-256">Requirement</span></span> | <span data-ttu-id="a0f48-257">值</span><span class="sxs-lookup"><span data-stu-id="a0f48-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f48-258">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0f48-258">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f48-259">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0f48-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0f48-260">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0f48-260">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f48-261">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0f48-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a0f48-262">標頭</span><span class="sxs-lookup"><span data-stu-id="a0f48-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f48-263"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a0f48-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




