---
description: PROPERTYINFO 資料結構會定義通訊協定的一個屬性。
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: 'PROPERTYINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943984"
---
# <a name="propertyinfo-structure"></a><span data-ttu-id="110d9-103">PROPERTYINFO 結構</span><span class="sxs-lookup"><span data-stu-id="110d9-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="110d9-104">**PROPERTYINFO** 資料結構會定義通訊協定的一個屬性。</span><span class="sxs-lookup"><span data-stu-id="110d9-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="110d9-105">語法</span><span class="sxs-lookup"><span data-stu-id="110d9-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a><span data-ttu-id="110d9-106">成員</span><span class="sxs-lookup"><span data-stu-id="110d9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="110d9-107">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="110d9-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-108">將此欄位設定為零。</span><span class="sxs-lookup"><span data-stu-id="110d9-108">Set this field to zero.</span></span> <span data-ttu-id="110d9-109">在輸出中，網路監視器會在屬性加入至屬性資料庫之後，傳回屬性的控制碼。</span><span class="sxs-lookup"><span data-stu-id="110d9-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="110d9-110">**版本**</span><span class="sxs-lookup"><span data-stu-id="110d9-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="110d9-111">Reserved.</span></span> <span data-ttu-id="110d9-112">必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="110d9-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="110d9-113">**標籤**</span><span class="sxs-lookup"><span data-stu-id="110d9-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-114">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="110d9-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="110d9-115">**註解**</span><span class="sxs-lookup"><span data-stu-id="110d9-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-116">屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="110d9-116">Description of the property.</span></span> <span data-ttu-id="110d9-117">描述會顯示在網路監視器狀態列上。</span><span class="sxs-lookup"><span data-stu-id="110d9-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="110d9-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="110d9-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-119">屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="110d9-119">Data type of the property.</span></span> <span data-ttu-id="110d9-120">這個成員可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="110d9-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="110d9-121">值</span><span class="sxs-lookup"><span data-stu-id="110d9-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="110d9-122">意義</span><span class="sxs-lookup"><span data-stu-id="110d9-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="110d9-123"><dt>**\_類型 VOID 的類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="110d9-124">屬性類型未知。</span><span class="sxs-lookup"><span data-stu-id="110d9-124">Property type is unknown.</span></span> <span data-ttu-id="110d9-125">沒有默示的長度或格式。</span><span class="sxs-lookup"><span data-stu-id="110d9-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="110d9-126"><dt>**\_類型 \_ 摘要**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="110d9-127">摘要屬性型別。</span><span class="sxs-lookup"><span data-stu-id="110d9-127">Summarizing property type.</span></span> <span data-ttu-id="110d9-128">指出剖析器附加至框架的第一個屬性實例。</span><span class="sxs-lookup"><span data-stu-id="110d9-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="110d9-129">\_屬性類型 \_ 摘要可作為屬性群組的預留位置。</span><span class="sxs-lookup"><span data-stu-id="110d9-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="110d9-130">此值指出未在通訊協定 *RFC* 中定義屬性。</span><span class="sxs-lookup"><span data-stu-id="110d9-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="110d9-131"><dt>**\_型別 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="110d9-132">大小為一個位元組 (8 位實體) 的數值資料。</span><span class="sxs-lookup"><span data-stu-id="110d9-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="110d9-133"><dt>**\_類型 \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="110d9-134">大小為兩個位元組的數值資料 (16 位實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="110d9-135"><dt>**\_類型 DWORD 的類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="110d9-136">大小為四個位元組的數值資料 (32 位實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="110d9-137"><dt>**\_LARGEINT 類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="110d9-138">大小為8個位元組的數值資料 (64 位實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="110d9-139"><dt>**\_類型 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="110d9-140">MAC 位址 (6 個位元組的實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="110d9-141"><dt>**\_類型時間的類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="110d9-142">**SYSTEMTIME** 結構。</span><span class="sxs-lookup"><span data-stu-id="110d9-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="110d9-143"><dt>**\_類型 \_ 字串類型字串**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="110d9-144">ASCII 文字資料。</span><span class="sxs-lookup"><span data-stu-id="110d9-144">ASCII text data.</span></span> <span data-ttu-id="110d9-145">這種資料類型不是以 Null 結束。</span><span class="sxs-lookup"><span data-stu-id="110d9-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="110d9-146">若為 Unicode 資料，當指定了 ASCII 文字資料時， \_ 當呼叫 attach 屬性實例函式時，也必須設定 IFLAG Unicode 旗標。</span><span class="sxs-lookup"><span data-stu-id="110d9-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="110d9-147"><dt>**\_型別 \_ IP \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="110d9-148">IP 位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-148">IP Address.</span></span> <span data-ttu-id="110d9-149"> (4 位元組的實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="110d9-150"><dt>**\_型別 \_ IPX \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="110d9-151">IPX 位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-151">IPX Address.</span></span> <span data-ttu-id="110d9-152"> (10 位元組的實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="110d9-153"><dt>**\_ \_ BYTESWAPPED WORD 的型別 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="110d9-154">已過時。</span><span class="sxs-lookup"><span data-stu-id="110d9-154">Obsolete.</span></span> <span data-ttu-id="110d9-155">若為位元組交換的單字資料，請將 **DataType** 設定為屬性 \_ 類型 \_ WORD，並 \_ 在呼叫 **附加** 屬性實例函數時設定 IFLAG 交換旗標。</span><span class="sxs-lookup"><span data-stu-id="110d9-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="110d9-156"><dt>**\_ \_ BYTESWAPPED DWORD 的型別 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="110d9-157">已過時。</span><span class="sxs-lookup"><span data-stu-id="110d9-157">Obsolete.</span></span> <span data-ttu-id="110d9-158">若為位元組交換的 DWORD 資料，請將 **DataType** 設定為屬性 \_ 類型 \_ dword，並 \_ 在呼叫 **附加** 屬性實例函數時設定 IFLAG 交換旗標。</span><span class="sxs-lookup"><span data-stu-id="110d9-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="110d9-159"><dt>**\_類型 \_ 字串類型 \_ 字串**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="110d9-160">已過時。</span><span class="sxs-lookup"><span data-stu-id="110d9-160">Obsolete.</span></span> <span data-ttu-id="110d9-161">若為變數類型的字串資料，請將 **DataType** 設定為屬性 \_ 類型 \_ 字串，並 \_ 在呼叫 **附加** 屬性實例函數時設定 IFLAG UNICODE 旗標。</span><span class="sxs-lookup"><span data-stu-id="110d9-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="110d9-162"><dt>**\_類型 \_ 原始 \_ 資料的類型**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="110d9-163">未知長度和格式的原始資料。</span><span class="sxs-lookup"><span data-stu-id="110d9-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="110d9-164"><dt>**\_型別 \_ 批註**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="110d9-165">與型別 \_ \_ VOID 相同。</span><span class="sxs-lookup"><span data-stu-id="110d9-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="110d9-166"><dt>**\_SRCFRIENDLYNAME 類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="110d9-167">來源易記名稱的位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-167">Address of source-friendly name.</span></span> <span data-ttu-id="110d9-168">網路監視器不會提供此資料類型的內建格式支援。</span><span class="sxs-lookup"><span data-stu-id="110d9-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="110d9-169"><dt>**\_DSTFRIENDLYNAME 類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="110d9-170">目的地易記名稱的位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-170">Address of destination friendly name.</span></span> <span data-ttu-id="110d9-171">網路監視器不會提供此資料類型的內建格式支援。</span><span class="sxs-lookup"><span data-stu-id="110d9-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="110d9-172"><dt>**\_ \_ TOKENRING 位址的 \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="110d9-173">權杖-環形位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-173">Token-ring address.</span></span> <span data-ttu-id="110d9-174">網路監視器不會提供此資料類型的內建格式支援。</span><span class="sxs-lookup"><span data-stu-id="110d9-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="110d9-175"><dt>**\_類型的 \_ FDDI \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="110d9-176">FDDI 位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-176">FDDI address.</span></span> <span data-ttu-id="110d9-177">網路監視器不會提供此資料類型的內建格式支援。</span><span class="sxs-lookup"><span data-stu-id="110d9-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="110d9-178"><dt>**\_類型 \_ 乙太網路 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="110d9-179">乙太網路位址。</span><span class="sxs-lookup"><span data-stu-id="110d9-179">Ethernet address.</span></span> <span data-ttu-id="110d9-180">網路監視器不會提供此資料類型的內建格式支援。</span><span class="sxs-lookup"><span data-stu-id="110d9-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="110d9-181"><dt>**\_型別 \_ 物件 \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="110d9-182">BER 編碼的 SNMP 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="110d9-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="110d9-183"><dt>**\_ \_ VINES \_ IP 位址的 \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="110d9-184">Vines IP 位址 (6 位元組實體) 。</span><span class="sxs-lookup"><span data-stu-id="110d9-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="110d9-185"><dt>**\_型別 \_ VAR \_ LEN \_ SMALL \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="110d9-186">數值沒有預先決定的長度，但長度不超過8個位元組。</span><span class="sxs-lookup"><span data-stu-id="110d9-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="110d9-187">附加資料的長度會決定值的長度。</span><span class="sxs-lookup"><span data-stu-id="110d9-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="110d9-188">**DataQualifier**</span><span class="sxs-lookup"><span data-stu-id="110d9-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-189">屬性的資料辨識符號。</span><span class="sxs-lookup"><span data-stu-id="110d9-189">The data qualifier of a property.</span></span> <span data-ttu-id="110d9-190">此成員提供資料類型的精確資訊。</span><span class="sxs-lookup"><span data-stu-id="110d9-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="110d9-191">**DataQualifier** 可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="110d9-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="110d9-192">值</span><span class="sxs-lookup"><span data-stu-id="110d9-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="110d9-193">意義</span><span class="sxs-lookup"><span data-stu-id="110d9-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="110d9-194"><dt>**\_QUAL \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="110d9-195">屬性資料類型是唯一的屬性規格。</span><span class="sxs-lookup"><span data-stu-id="110d9-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="110d9-196">當設定此值時，結構的聯集成員會設定為 **Null**，然後予以忽略。</span><span class="sxs-lookup"><span data-stu-id="110d9-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="110d9-197"><dt>**\_QUAL \_ 範圍的範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="110d9-198">數值應該在指定的範圍內。</span><span class="sxs-lookup"><span data-stu-id="110d9-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="110d9-199">定義 **lpRange** 成員中的範圍。</span><span class="sxs-lookup"><span data-stu-id="110d9-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="110d9-200"><dt>**配置 \_ QUAL \_ 集**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="110d9-201">屬性的值會與在結構聯集的 **lpSet** 成員中指定的一組值進行比較。</span><span class="sxs-lookup"><span data-stu-id="110d9-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="110d9-202">屬性的值可以是 **位元組**、 **字** 組、 **DWORD**、 **LARGEINT** 或 **時間**。</span><span class="sxs-lookup"><span data-stu-id="110d9-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="110d9-203"><dt>**QUAL 位欄位 \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="110d9-204">已過時。</span><span class="sxs-lookup"><span data-stu-id="110d9-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="110d9-205"><dt>**\_QUAL \_ 標記的 \_ 設定**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="110d9-206">屬性值會與一組值標籤配對中的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="110d9-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="110d9-207">值標籤組是在結構聯集的 **lpSet** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="110d9-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="110d9-208">在顯示時間，如果屬性的值符合集合中的值，則會顯示值和相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="110d9-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="110d9-209"><dt>**\_QUAL \_ 標記的位欄位 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="110d9-210">已過時。</span><span class="sxs-lookup"><span data-stu-id="110d9-210">Obsolete.</span></span> <span data-ttu-id="110d9-211">請改用 \_ QUAL \_ 旗標。</span><span class="sxs-lookup"><span data-stu-id="110d9-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="110d9-212"><dt>**\_QUAL \_ CONST 的**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="110d9-213">屬性的值會與位在 union 的 **value** 成員中指定的常數進行比較。</span><span class="sxs-lookup"><span data-stu-id="110d9-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="110d9-214">在顯示時間，如果屬性值和常數不相符，則會出現格式化的錯誤訊息，並將值設定為 [一般]。</span><span class="sxs-lookup"><span data-stu-id="110d9-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="110d9-215"><dt>**\_QUAL \_ 旗標的**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="110d9-216">屬性的值會與位在聯集的 **lpSet** 成員中識別的特定位進行比較。</span><span class="sxs-lookup"><span data-stu-id="110d9-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="110d9-217"><dt>**\_QUAL \_ 陣列的**</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="110d9-218">屬性的值會指定值的陣列。</span><span class="sxs-lookup"><span data-stu-id="110d9-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="110d9-219">附加資料的長度會決定陣列的長度。</span><span class="sxs-lookup"><span data-stu-id="110d9-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="110d9-220">當設定了 \_ QUAL \_ 陣列值的成員時， **PROPERTYINFO** 資料結構的聯集成員會設定為 **Null** 並忽略。</span><span class="sxs-lookup"><span data-stu-id="110d9-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="110d9-221">**lpExtendedInfo**</span><span class="sxs-lookup"><span data-stu-id="110d9-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-222">Union) 的保留 (成員。</span><span class="sxs-lookup"><span data-stu-id="110d9-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="110d9-223">**lpRange**</span><span class="sxs-lookup"><span data-stu-id="110d9-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-224">定義值範圍的 [範圍](range.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="110d9-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="110d9-225">如果這個結構的 **DataQualifier** 成員設定為 \_ \_ union)  (成員，則必須設定這個成員。</span><span class="sxs-lookup"><span data-stu-id="110d9-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="110d9-226">**lpSet**</span><span class="sxs-lookup"><span data-stu-id="110d9-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-227">指定一組值或標籤之 [集合](set.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="110d9-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="110d9-228">如果結構的 **DataQualifier** 成員設定為 [ \_ QUAL \_ 集]、[ \_ QUAL 標記集] 或 [配置 QUAL] \_ \_ 旗標 \_ \_ () 成員，則必須設定這個成員。</span><span class="sxs-lookup"><span data-stu-id="110d9-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="110d9-229">**特**</span><span class="sxs-lookup"><span data-stu-id="110d9-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-230">Union) 的已淘汰 (成員。</span><span class="sxs-lookup"><span data-stu-id="110d9-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="110d9-231">**值**</span><span class="sxs-lookup"><span data-stu-id="110d9-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-232">當 **DataQualifier** 設定為 \_ QUAL \_ CONST (union) 成員時，所使用的常數值。</span><span class="sxs-lookup"><span data-stu-id="110d9-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="110d9-233">**FormatStringSize**</span><span class="sxs-lookup"><span data-stu-id="110d9-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-234">只用于屬性描述的大小上限。</span><span class="sxs-lookup"><span data-stu-id="110d9-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="110d9-235">**InstanceData**</span><span class="sxs-lookup"><span data-stu-id="110d9-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="110d9-236">指定格式化函數，這個函數會呼叫以格式化屬性的顯示資料。</span><span class="sxs-lookup"><span data-stu-id="110d9-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="110d9-237">若要使用一般格式子，請指定 **FormatPropertyInstance** 函數。</span><span class="sxs-lookup"><span data-stu-id="110d9-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="110d9-238">備註</span><span class="sxs-lookup"><span data-stu-id="110d9-238">Remarks</span></span>

<span data-ttu-id="110d9-239">**PROPERTYINFO** 結構是用來呼叫 [AddProperty](/previous-versions/bb251873(v=msdn.10))函數。</span><span class="sxs-lookup"><span data-stu-id="110d9-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="110d9-240">**AddProperty** 函數會將單一屬性定義加入至剖析器 [*屬性資料庫*](p.md)。</span><span class="sxs-lookup"><span data-stu-id="110d9-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="110d9-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="110d9-241">Requirements</span></span>



| <span data-ttu-id="110d9-242">需求</span><span class="sxs-lookup"><span data-stu-id="110d9-242">Requirement</span></span> | <span data-ttu-id="110d9-243">值</span><span class="sxs-lookup"><span data-stu-id="110d9-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="110d9-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="110d9-244">Minimum supported client</span></span><br/> | <span data-ttu-id="110d9-245">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="110d9-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="110d9-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="110d9-246">Minimum supported server</span></span><br/> | <span data-ttu-id="110d9-247">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="110d9-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="110d9-248">標頭</span><span class="sxs-lookup"><span data-stu-id="110d9-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="110d9-249"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="110d9-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="110d9-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="110d9-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="110d9-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="110d9-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="110d9-252">範圍</span><span class="sxs-lookup"><span data-stu-id="110d9-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="110d9-253">SET</span><span class="sxs-lookup"><span data-stu-id="110d9-253">SET</span></span>](set.md)
</dt> </dl>

 

