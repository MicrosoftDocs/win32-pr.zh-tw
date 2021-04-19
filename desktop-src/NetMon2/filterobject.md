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
# <a name="filterobject-structure"></a>FILTEROBJECT 結構

**FILTEROBJECT** 結構會定義顯示篩選的單一物件。 [**FilterAddObject**](filteraddobject.md)函數會使用 **FILTEROBJECT** 來建立顯示篩選。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**動作**
</dt> <dd>

指定 **FILTEROBJECT** 動作的旗標。 旗標可以指定屬性、值或運算子。

下表列出動作成員屬性旗標。



| 值                                                                                                                                                                                                | 意義                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**FILTERACTION \_ 屬性**</dt> </dl>                | 包含這個屬性。<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**FILTERACTION \_ PROPERTYEXIST**</dt> </dl> | 表示已定義篩選動作屬性。<br/> |



 

下表列出動作成員值旗標。



| 值                                                                                                                                                                                        | 意義                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**FILTERACTION \_ 值**</dt> </dl>                 | 包含這個值。<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**FILTERACTION \_ 字串**</dt> </dl>              | 包含這個字串。<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**FILTERACTION \_ 陣列**</dt> </dl>                 | 包含此陣列。<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**FILTERACTION \_ CONTAINSNC**</dt> </dl>  | 指出屬性包含不區分大小寫的子字串。<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**FILTERACTION \_ CONTAINS**</dt> </dl>        | 指出屬性包含區分大小寫的子字串。<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**FILTERACTION \_ 位址**</dt> </dl>           | 包含 MAC 位址。<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**FILTERACTION \_ ADDRESSANY**</dt> </dl>  | 符合任何 MAC 位址。<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**FILTERACTION \_ 來源**</dt> </dl>                    | 表示 **從 MAC** 位址。<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**FILTERACTION \_ 至**</dt> </dl>                          | 表示 **至 MAC** 位址。<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**FILTERACTION \_ FROMTO**</dt> </dl>              | 表示與 MAC 位址的 **之間** 的配對。<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**FILTERACTION \_ LARGEINT**</dt> </dl>        | 包含大整數。<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**FILTERACTION \_ TIME**</dt> </dl>                    | 包含 **SYSTEMTIME** 結構。<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**FILTERACTION \_ ADDR \_ 乙太幣**</dt> </dl> | 包含乙太網路 MAC 位址。<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**FILTERACTION \_ 位址 \_ 權杖**</dt> </dl> | 包含權杖環形 MAC 位址。<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**FILTERACTION \_ ADDR 的 \_ FDDI**</dt> </dl>    | 包含 FDDI MAC 位址。<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**FILTERACTION \_ 位址 \_ IPX**</dt> </dl>       | 包含 IPX MAC 位址。<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**FILTERACTION \_ 位址 \_ IP**</dt> </dl>          | 包含 IP MAC 位址。<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**FILTERACTION \_ OID**</dt> </dl>                       | 包含 (OID) 的物件識別碼。<br/>                             |



 

下表列出動作成員運算子旗標。



| 值                                                                                                                                                                                                        | 意義                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**FILTERACTION \_ 無效**</dt> </dl>                           | 指出不正確篩選動作。<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERACTION \_ 和**</dt> </dl>                                       | 表示邏輯 **AND** 語句。<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERACTION \_ 或**</dt> </dl>                                          | 表示邏輯 **OR** 語句。<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**FILTERACTION \_ XOR**</dt> </dl>                                       | 表示邏輯互斥 **OR** (XOR) 語句。<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**FILTERACTION \_ NOT**</dt> </dl>                                       | 表示邏輯 **NOT** 語句。<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**FILTERACTION \_ EQUALNC**</dt> </dl>                           | 篩選動作相等且不區分大小寫。<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**FILTERACTION \_ 相等**</dt> </dl>                                 | 篩選動作相等且區分大小寫。<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**FILTERACTION \_ NOTEQUALNC**</dt> </dl>                  | 邏輯 **NOT** 語句相等且不區分大小寫。<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**FILTERACTION \_ NOTEQUAL**</dt> </dl>                        | 邏輯 **NOT** 語句相等，而且區分大小寫。<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**FILTERACTION \_ GREATERNC**</dt> </dl>                     | 篩選動作大於 (>) ，且不區分大小寫。<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**FILTERACTION \_ 更多**</dt> </dl>                           | 篩選動作大於 (>) 和區分大小寫。<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**FILTERACTION \_ LESSNC**</dt> </dl>                              | 篩選動作小於 (<) ，且不區分大小寫。<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**\_LESS 篩選**</dt> </dl>                                    | 篩選動作小於 (<) 和區分大小寫。<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**FILTERACTION \_ GREATEREQUALNC**</dt> </dl>      | 篩選動作大於或等於 (>=) 且不區分大小寫。<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**FILTERACTION \_ GREATEREQUAL**</dt> </dl>            | 篩選動作大於或等於 (>=) 和區分大小寫。<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**FILTERACTION \_ LESSEQUALNC**</dt> </dl>               | 篩選動作小於或等於 (<=) 且不區分大小寫。<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**FILTERACTION \_ LESSEQUAL**</dt> </dl>                     | 篩選動作小於或等於 (<=) ，而且會區分大小寫。<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**FILTERACTION \_ PLUS**</dt> </dl>                                    | 將運算子新增 (+) 。<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**FILTERACTION \_ 減號**</dt> </dl>                                 | 減去運算子 (-) 。<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**FILTERACTION \_ AREBITSON**</dt> </dl>                     | 表示位運算。<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**FILTERACTION \_ AREBITSOFF**</dt> </dl>                  | 表示非位運算。<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt> </dl>      | 表示選取的通訊協定存在。<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLEXIST**</dt> </dl>         | 表示選取的通訊協定存在。<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**FILTERACTION \_ ARRAYEQUAL**</dt> </dl>                  | 指出陣列內容相等。 旗標必須與 **FILTERACTION \_ 陣列** 結構一起使用。<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**FILTERACTION \_ DEREFPROPERTY**</dt> </dl>         | 描述從通訊協定到位移 (位元組) 的模式比對。<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**FILTERACTION \_ OID \_ CONTAINS**</dt> </dl>           | 評估物件識別碼內的子字串。 動作必須與 **FILTERACTION \_ OID** 結構一起使用。<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**FILTERACTION \_ OID \_ 開頭 \_ 為**</dt> </dl> | 評估開始物件識別碼的子字串。 旗標必須與 **FILTERACTION \_ OID** 一起使用。<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**FILTERACTION \_ OID \_ 結尾 \_ 為**</dt> </dl>       | 評估結束物件識別碼的子字串。 旗標必須與 **FILTERACTION \_ OID** 一起使用。<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**FILTERACTION \_ ADDR \_ VINES**</dt> </dl>                 | 包含 Vines MAC 位址。<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**FILTERACTION \_ 運算式**</dt> </dl>                  | 包含動作運算式。<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**FILTERACTION \_ BOOL**</dt> </dl>                                    | 包含 **BOOL** 資料類型。<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**\_ \_ 接下來的篩選方向**</dt> </dl>                       | 控制在捕捉檔案內 (下一個框架) 的順序方向。<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**\_前篩選方向 \_**</dt> </dl>                       | 控制在捕獲檔案內 (上一個框架) 的順序方向。<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

屬性索引鍵的控制碼。

</dd> <dt>

**值**
</dt> <dd>

物件的值。

</dd> <dt>

**hProtocol**
</dt> <dd>

顯示篩選器通訊協定的控制碼。

</dd> <dt>

**lpArray**
</dt> <dd>

陣列的指標。

</dd> <dt>

**lpProtocolTable**
</dt> <dd>

通訊協定清單的指標，其設計目的是要測試框架中的通訊協定是否存在。

</dd> <dt>

**lpAddress**
</dt> <dd>

核心類型位址的指標。 例如，MAC 或 IP。

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Windows NT 或 Windows 2000 應用程式中使用的雙 **DWORD** 。

</dd> <dt>

**lpTime**
</dt> <dd>

**SYSTEMTIME** 結構的指標。

</dd> <dt>

**lpOID**
</dt> <dd>

**物件 \_ 識別碼** 的指標， (OID) 結構。

</dd> <dt>

**ByteCount**
</dt> <dd>

框架中的數位（以位元組為單位）。

</dd> <dt>

**ByteOffset**
</dt> <dd>

用來比較陣列的 FILTEROBJECT 結構的位移位元組值。

</dd> <dt>

**pNext**
</dt> <dd>

保留的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




