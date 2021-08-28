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
ms.openlocfilehash: 8dc20b94fbf889b4c04712eadbee5d7d834d3cf260962fe01ef7837e5893c4a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128948"
---
# <a name="propertyinfo-structure"></a>PROPERTYINFO 結構

**PROPERTYINFO** 資料結構會定義通訊協定的一個屬性。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**hProperty**
</dt> <dd>

將此欄位設定為零。 在輸出中，網路監視器會在屬性加入至屬性資料庫之後，傳回屬性的控制碼。

</dd> <dt>

**版本**
</dt> <dd>

保留的。 必須設定為零。

</dd> <dt>

**標籤**
</dt> <dd>

屬性的名稱。

</dd> <dt>

**註解**
</dt> <dd>

屬性的描述。 描述會顯示在網路監視器狀態列上。

</dd> <dt>

**DataType**
</dt> <dd>

屬性的資料類型。 這個成員可以具有下列其中一個值。



| 值                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**\_類型 VOID 的類型 \_**</dt> </dl>                                           | 屬性類型未知。 沒有默示的長度或格式。<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**\_類型 \_ 摘要**</dt> </dl>                                  | 摘要屬性型別。 指出剖析器附加至框架的第一個屬性實例。 \_屬性類型 \_ 摘要可作為屬性群組的預留位置。 此值指出未在通訊協定 *RFC* 中定義屬性。<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**\_型別 \_ 位元組**</dt> </dl>                                           | 大小為一個位元組 (8 位實體) 的數值資料。<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**\_類型 \_ 文字**</dt> </dl>                                           | 大小為兩個位元組的數值資料 (16 位實體) 。<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**\_類型 DWORD 的類型 \_**</dt> </dl>                                        | 大小為四個位元組的數值資料 (32 位實體) 。<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**\_LARGEINT 類型 \_**</dt> </dl>                               | 大小為8個位元組的數值資料 (64 位實體) 。<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**\_類型 \_ 位址**</dt> </dl>                                           | MAC 位址 (6 個位元組的實體) 。<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**\_類型時間的類型 \_**</dt> </dl>                                           | **SYSTEMTIME** 結構。<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**\_類型 \_ 字串類型字串**</dt> </dl>                                     | ASCII 文字資料。 這種資料類型不是以 Null 結束。 <br/> 若為 Unicode 資料，當指定了 ASCII 文字資料時， \_ 當呼叫 attach 屬性實例函式時，也必須設定 IFLAG Unicode 旗標。<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**\_型別 \_ IP \_ 位址**</dt> </dl>                        | IP 位址。  (4 位元組的實體) 。<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**\_型別 \_ IPX \_ 位址**</dt> </dl>                     | IPX 位址。  (10 位元組的實體) 。<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**\_ \_ BYTESWAPPED WORD 的型別 \_**</dt> </dl>      | 已過時。 若為位元組交換的單字資料，請將 **DataType** 設定為屬性 \_ 類型 \_ WORD，並 \_ 在呼叫 **附加** 屬性實例函數時設定 IFLAG 交換旗標。<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**\_ \_ BYTESWAPPED DWORD 的型別 \_**</dt> </dl>   | 已過時。 若為位元組交換的 DWORD 資料，請將 **DataType** 設定為屬性 \_ 類型 \_ dword，並 \_ 在呼叫 **附加** 屬性實例函數時設定 IFLAG 交換旗標。<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**\_類型 \_ 字串類型 \_ 字串**</dt> </dl>                  | 已過時。 若為變數類型的字串資料，請將 **DataType** 設定為屬性 \_ 類型 \_ 字串，並 \_ 在呼叫 **附加** 屬性實例函數時設定 IFLAG UNICODE 旗標。<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**\_類型 \_ 原始 \_ 資料的類型**</dt> </dl>                              | 未知長度和格式的原始資料。<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**\_型別 \_ 批註**</dt> </dl>                                  | 與型別 \_ \_ VOID 相同。<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**\_SRCFRIENDLYNAME 類型 \_**</dt> </dl>          | 來源易記名稱的位址。 網路監視器不會提供此資料類型的內建格式支援。<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**\_DSTFRIENDLYNAME 類型 \_**</dt> </dl>          | 目的地易記名稱的位址。 網路監視器不會提供此資料類型的內建格式支援。<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**\_ \_ TOKENRING 位址的 \_ 類型**</dt> </dl>   | 權杖-環形位址。 網路監視器不會提供此資料類型的內建格式支援。<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**\_類型的 \_ FDDI \_ 位址**</dt> </dl>                  | FDDI 位址。 網路監視器不會提供此資料類型的內建格式支援。<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**\_類型 \_ 乙太網路 \_ 位址**</dt> </dl>      | 乙太網路位址。 網路監視器不會提供此資料類型的內建格式支援。<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**\_型別 \_ 物件 \_ 識別碼**</dt> </dl>   | BER 編碼的 SNMP 物件識別碼。<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**\_ \_ VINES \_ IP 位址的 \_ 類型**</dt> </dl>     | Vines IP 位址 (6 位元組實體) 。<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**\_型別 \_ VAR \_ LEN \_ SMALL \_ INT**</dt> </dl> | 數值沒有預先決定的長度，但長度不超過8個位元組。 附加資料的長度會決定值的長度。<br/>                                                                                                                                                |



 

</dd> <dt>

**DataQualifier**
</dt> <dd>

屬性的資料辨識符號。 此成員提供資料類型的精確資訊。

**DataQualifier** 可以具有下列其中一個值。



| 值                                                                                                                                                                                                  | 意義                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**\_QUAL \_ 無**</dt> </dl>                                      | 屬性資料類型是唯一的屬性規格。 <br/> 當設定此值時，結構的聯集成員會設定為 **Null**，然後予以忽略。<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**\_QUAL \_ 範圍的範圍**</dt> </dl>                                   | 數值應該在指定的範圍內。 定義 **lpRange** 成員中的範圍。<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**配置 \_ QUAL \_ 集**</dt> </dl>                                         | 屬性的值會與在結構聯集的 **lpSet** 成員中指定的一組值進行比較。 屬性的值可以是 **位元組**、 **字** 組、 **DWORD**、 **LARGEINT** 或 **時間**。<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**QUAL 位欄位 \_ \_**</dt> </dl>                          | 已過時。<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**\_QUAL \_ 標記的 \_ 設定**</dt> </dl>                | 屬性值會與一組值標籤配對中的值進行比較。 值標籤組是在結構聯集的 **lpSet** 成員中指定的。 <br/> 在顯示時間，如果屬性的值符合集合中的值，則會顯示值和相關聯的標籤。<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**\_QUAL \_ 標記的位欄位 \_**</dt> </dl> | 已過時。 請改用 \_ QUAL \_ 旗標。<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**\_QUAL \_ CONST 的**</dt> </dl>                                   | 屬性的值會與位在 union 的 **value** 成員中指定的常數進行比較。 <br/> 在顯示時間，如果屬性值和常數不相符，則會出現格式化的錯誤訊息，並將值設定為 [一般]。<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**\_QUAL \_ 旗標的**</dt> </dl>                                   | 屬性的值會與位在聯集的 **lpSet** 成員中識別的特定位進行比較。<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**\_QUAL \_ 陣列的**</dt> </dl>                                   | 屬性的值會指定值的陣列。 附加資料的長度會決定陣列的長度。 <br/> 當設定了 \_ QUAL \_ 陣列值的成員時， **PROPERTYINFO** 資料結構的聯集成員會設定為 **Null** 並忽略。<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Union) 的保留 (成員。

</dd> <dt>

**lpRange**
</dt> <dd>

定義值範圍的 [範圍](range.md) 結構指標。 如果這個結構的 **DataQualifier** 成員設定為 \_ \_ union)  (成員，則必須設定這個成員。

</dd> <dt>

**lpSet**
</dt> <dd>

指定一組值或標籤之 [集合](set.md) 結構的指標。 如果結構的 **DataQualifier** 成員設定為 [ \_ QUAL \_ 集]、[ \_ QUAL 標記集] 或 [配置 QUAL] \_ \_ 旗標 \_ \_ () 成員，則必須設定這個成員。

</dd> <dt>

**特**
</dt> <dd>

Union) 的已淘汰 (成員。

</dd> <dt>

**值**
</dt> <dd>

當 **DataQualifier** 設定為 \_ QUAL \_ CONST (union) 成員時，所使用的常數值。

</dd> <dt>

**FormatStringSize**
</dt> <dd>

只用于屬性描述的大小上限。

</dd> <dt>

**InstanceData**
</dt> <dd>

指定格式化函數，這個函數會呼叫以格式化屬性的顯示資料。 若要使用一般格式子，請指定 **FormatPropertyInstance** 函數。

</dd> </dl>

## <a name="remarks"></a>備註

**PROPERTYINFO** 結構是用來呼叫 [AddProperty](/previous-versions/bb251873(v=msdn.10))函數。 **AddProperty** 函數會將單一屬性定義加入至剖析器 [*屬性資料庫*](p.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[範圍](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

