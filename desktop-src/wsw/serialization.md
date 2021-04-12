---
title: 序列化
description: 序列化是將 C 資料結構中的值寫入 (結構、陣列和基本值) 為 XML 元素的程式。 還原序列化是反向處理。
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- 適用于 Windows 的序列化 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104195694"
---
# <a name="serialization"></a><span data-ttu-id="db900-107">序列化</span><span class="sxs-lookup"><span data-stu-id="db900-107">Serialization</span></span>

<span data-ttu-id="db900-108">序列化是將 C 資料結構中的值寫入 (結構、陣列和基本值) 為 XML 元素的程式。</span><span class="sxs-lookup"><span data-stu-id="db900-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="db900-109">還原序列化是反向處理。</span><span class="sxs-lookup"><span data-stu-id="db900-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="db900-110">序列化是將 C 資料結構中的值寫入 (結構、陣列和基本值) 為 XML 元素的程式。</span><span class="sxs-lookup"><span data-stu-id="db900-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="db900-111">還原序列化是反向處理。</span><span class="sxs-lookup"><span data-stu-id="db900-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="db900-112">這兩個處理常式都依賴 C 資料結構與 XML 之間的對應描述。</span><span class="sxs-lookup"><span data-stu-id="db900-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![圖表顯示序列化和還原序列化如何依賴 C 資料結構與 XML 之間的對應描述。](images/xmlmapping.png)

<span data-ttu-id="db900-114">為了序列化值，應用程式會呼叫 [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)、 [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) 或 [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)。</span><span class="sxs-lookup"><span data-stu-id="db900-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="db900-115">若要還原序列化值，應用程式會呼叫 [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)、 [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) 或 [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)。</span><span class="sxs-lookup"><span data-stu-id="db900-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="db900-116">安全性</span><span class="sxs-lookup"><span data-stu-id="db900-116">Security</span></span>

<span data-ttu-id="db900-117">[XML 讀取器](xml-reader.md) 用於還原序列化進程。</span><span class="sxs-lookup"><span data-stu-id="db900-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="db900-118">請參閱 XML 讀取器中的安全性一節，以取得 XML 相關的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="db900-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="db900-119">還原序列化程式會繼續還原序列化資料，直到它完成讀取還原序列化的專案為止。</span><span class="sxs-lookup"><span data-stu-id="db900-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="db900-120">當還原序列化程式遇到任何不符合正在還原序列化之資料描述的 XML 檔時，就會失敗。</span><span class="sxs-lookup"><span data-stu-id="db900-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="db900-121">在該時間點，使用的 XML 讀取器變成無效，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="db900-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="db900-122">根據預設，還原序列化是 strict。</span><span class="sxs-lookup"><span data-stu-id="db900-122">By default deserialization is strict.</span></span> <span data-ttu-id="db900-123">導致還原序列化失敗的某些情況，包括但不限於：</span><span class="sxs-lookup"><span data-stu-id="db900-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="db900-124">遺漏預期的元素</span><span class="sxs-lookup"><span data-stu-id="db900-124">Expected elements is missing</span></span>
-   <span data-ttu-id="db900-125">必要元素之間出現非預期的專案欄位</span><span class="sxs-lookup"><span data-stu-id="db900-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="db900-126">必要欄位之後的額外元素內容，除非 **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="db900-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="db900-127">除非指定 [**WS \_ 結構 \_ 忽略 \_ 未處理的 \_ 屬性**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) 旗標，否則未預期的屬性</span><span class="sxs-lookup"><span data-stu-id="db900-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="db900-128">超出指定範圍的非預期資料類型值</span><span class="sxs-lookup"><span data-stu-id="db900-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="db900-129">重複元素的計數超出指定的範圍</span><span class="sxs-lookup"><span data-stu-id="db900-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="db900-130">序列化大量資料可能會導致記憶體配置過多，而且可能會導致阻絕服務攻擊。</span><span class="sxs-lookup"><span data-stu-id="db900-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="db900-131">還原序列化資料的使用者必須指定堆積物件來配置資料，而且使用者可以使用堆積配置限制來防止記憶體配置攻擊。</span><span class="sxs-lookup"><span data-stu-id="db900-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="db900-132">資料類型的範圍支援，包括字串的最大長度、陣列中的最大專案計數等，可讓使用者控制不同資料類型的大小上限。</span><span class="sxs-lookup"><span data-stu-id="db900-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="db900-133">使用者可以在 [資料描述] 或 [架構] 中指定範圍，以限制不同資料的大小上限。</span><span class="sxs-lookup"><span data-stu-id="db900-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="db900-134">電傳格式支援包含內嵌零的字串值 (text、binary、MTOM) 。</span><span class="sxs-lookup"><span data-stu-id="db900-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="db900-135">當還原序列化具有內嵌零的字串時，使用者應該使用 (WS 字串的計數位符串 \_) 因此零不會混淆字串長度的計算。</span><span class="sxs-lookup"><span data-stu-id="db900-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="db900-136">如果將包含內嵌零的字串值還原序列化為預期以零結束字串的欄位，則會傳回錯誤，而且還原序列化會失敗。</span><span class="sxs-lookup"><span data-stu-id="db900-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="db900-137">如果使用 wsutil 來產生資料描述，則應使用/string： WS \_ string 選項，如果必須是具有內嵌零的字串。</span><span class="sxs-lookup"><span data-stu-id="db900-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="db900-138">下列回呼用於序列化：</span><span class="sxs-lookup"><span data-stu-id="db900-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="db900-139">**WS \_ 持續時間 \_ 比較 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="db900-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="db900-140">**WS \_ 讀取 \_ 類型 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="db900-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="db900-141">**WS \_ 寫入 \_ 類型 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="db900-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="db900-142">下列列舉用於序列化：</span><span class="sxs-lookup"><span data-stu-id="db900-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="db900-143">**WS \_ 欄位 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="db900-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="db900-144">**WS \_ 欄位 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="db900-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="db900-145">**WS \_ 讀取 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="db900-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="db900-146">**WS \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="db900-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="db900-147">**WS \_ 型別 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="db900-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="db900-148">**WS \_ 寫入 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="db900-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="db900-149">下列函式用於序列化：</span><span class="sxs-lookup"><span data-stu-id="db900-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="db900-150">**WsReadAttribute**</span><span class="sxs-lookup"><span data-stu-id="db900-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="db900-151">**WsReadElement**</span><span class="sxs-lookup"><span data-stu-id="db900-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="db900-152">**WsReadType**</span><span class="sxs-lookup"><span data-stu-id="db900-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="db900-153">**WsWriteAttribute**</span><span class="sxs-lookup"><span data-stu-id="db900-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="db900-154">**WsWriteElement**</span><span class="sxs-lookup"><span data-stu-id="db900-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="db900-155">**WsWriteType**</span><span class="sxs-lookup"><span data-stu-id="db900-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="db900-156">下列結構用於序列化：</span><span class="sxs-lookup"><span data-stu-id="db900-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="db900-157">**WS \_ 屬性 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="db900-158">**WS \_ BOOL \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="db900-159">**WS \_ 位元組 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="db900-160">**WS \_ 位元組 \_ 陣列 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="db900-161">**WS \_ 字元 \_ 陣列 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="db900-162">**WS \_ 自訂 \_ 類型 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="db900-163">**WS \_ DATETIME \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="db900-164">**WS \_ DECIMAL \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="db900-165">**WS \_ 預設 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="db900-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="db900-166">**WS \_ 雙重 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="db900-167">**WS \_ 持續時間 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="db900-168">**WS \_ 元素 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="db900-169">**WS \_ 端點 \_ 位址 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="db900-170">**WS \_ 列舉 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="db900-171">**WS \_ 列舉 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="db900-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="db900-172">**WS \_ 錯誤 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="db900-173">**WS \_ 欄位 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="db900-174">**WS \_ 浮點數 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="db900-175">**WS \_ GUID \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="db900-176">**WS \_ INT16 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="db900-177">**WS \_ INT32 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="db900-178">**WS \_ INT64 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="db900-179">**WS \_ INT8 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="db900-180">**WS \_ 專案 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="db900-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="db900-181">**WS \_ 字串 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="db900-182">**WS \_ 結構 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="db900-183">**WS \_ TIMESPAN \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="db900-184">**WS \_ UINT16 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="db900-185">**WS \_ UINT32 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="db900-186">**WS \_ UINT64 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="db900-187">**WS \_ UINT8 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="db900-188">**WS 聯 \_ 集 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="db900-189">**WS 聯 \_ 集 \_ 欄位 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="db900-190">**WS \_ 唯一 \_ 識別碼 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="db900-191">**WS \_ UTF8 \_ 陣列 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="db900-192">**WS \_ VOID \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="db900-193">**WS \_ WSZ \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="db900-194">**WS \_ XML \_ QNAME \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="db900-195">**WS \_ XML \_ 字串 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="db900-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




