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
# <a name="serialization"></a>序列化

序列化是將 C 資料結構中的值寫入 (結構、陣列和基本值) 為 XML 元素的程式。 還原序列化是反向處理。


序列化是將 C 資料結構中的值寫入 (結構、陣列和基本值) 為 XML 元素的程式。 還原序列化是反向處理。

這兩個處理常式都依賴 C 資料結構與 XML 之間的對應描述。

![圖表顯示序列化和還原序列化如何依賴 C 資料結構與 XML 之間的對應描述。](images/xmlmapping.png)

為了序列化值，應用程式會呼叫 [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)、 [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) 或 [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)。

若要還原序列化值，應用程式會呼叫 [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)、 [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) 或 [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)。

## <a name="security"></a>安全性

[XML 讀取器](xml-reader.md) 用於還原序列化進程。 請參閱 XML 讀取器中的安全性一節，以取得 XML 相關的安全性資訊。

還原序列化程式會繼續還原序列化資料，直到它完成讀取還原序列化的專案為止。 當還原序列化程式遇到任何不符合正在還原序列化之資料描述的 XML 檔時，就會失敗。 在該時間點，使用的 XML 讀取器變成無效，而且會傳回錯誤。

根據預設，還原序列化是 strict。 導致還原序列化失敗的某些情況，包括但不限於：

-   遺漏預期的元素
-   必要元素之間出現非預期的專案欄位
-   必要欄位之後的額外元素內容，除非 **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   除非指定 [**WS \_ 結構 \_ 忽略 \_ 未處理的 \_ 屬性**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) 旗標，否則未預期的屬性
-   超出指定範圍的非預期資料類型值
-   重複元素的計數超出指定的範圍

序列化大量資料可能會導致記憶體配置過多，而且可能會導致阻絕服務攻擊。 還原序列化資料的使用者必須指定堆積物件來配置資料，而且使用者可以使用堆積配置限制來防止記憶體配置攻擊。

資料類型的範圍支援，包括字串的最大長度、陣列中的最大專案計數等，可讓使用者控制不同資料類型的大小上限。 使用者可以在 [資料描述] 或 [架構] 中指定範圍，以限制不同資料的大小上限。

電傳格式支援包含內嵌零的字串值 (text、binary、MTOM) 。 當還原序列化具有內嵌零的字串時，使用者應該使用 (WS 字串的計數位符串 \_) 因此零不會混淆字串長度的計算。 如果將包含內嵌零的字串值還原序列化為預期以零結束字串的欄位，則會傳回錯誤，而且還原序列化會失敗。 如果使用 wsutil 來產生資料描述，則應使用/string： WS \_ string 選項，如果必須是具有內嵌零的字串。

下列回呼用於序列化：

-   [**WS \_ 持續時間 \_ 比較 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**WS \_ 讀取 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS \_ 寫入 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

下列列舉用於序列化：

-   [**WS \_ 欄位 \_ 對應**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**WS \_ 欄位 \_ 選項**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**WS \_ 讀取 \_ 選項**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**WS \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**WS \_ 型別 \_ 對應**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**WS \_ 寫入 \_ 選項**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

下列函式用於序列化：

-   [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

下列結構用於序列化：

-   [**WS \_ 屬性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**WS \_ BOOL \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**WS \_ 位元組 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**WS \_ 位元組 \_ 陣列 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**WS \_ 字元 \_ 陣列 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**WS \_ 自訂 \_ 類型 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**WS \_ DATETIME \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**WS \_ DECIMAL \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**WS \_ 預設 \_ 值**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**WS \_ 雙重 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**WS \_ 持續時間 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**WS \_ 端點 \_ 位址 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**WS \_ 列舉 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**WS \_ 列舉 \_ 值**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**WS \_ 錯誤 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**WS \_ 欄位 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**WS \_ 浮點數 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**WS \_ GUID \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**WS \_ INT16 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**WS \_ INT32 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**WS \_ INT64 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**WS \_ INT8 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**WS \_ 專案 \_ 範圍**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**WS \_ 字串 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**WS \_ 結構 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**WS \_ TIMESPAN \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**WS \_ UINT16 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**WS \_ UINT32 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**WS \_ UINT64 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**WS \_ UINT8 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**WS 聯 \_ 集 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**WS 聯 \_ 集 \_ 欄位 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**WS \_ 唯一 \_ 識別碼 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**WS \_ UTF8 \_ 陣列 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**WS \_ VOID \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**WS \_ WSZ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**WS \_ XML \_ QNAME \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**WS \_ XML \_ 字串 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




