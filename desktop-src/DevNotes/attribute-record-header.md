---
description: 表示屬性記錄。
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9664af36448bb125dc8d5fde3c4d22b04e58b1ca341acad561b94708acbf143c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045385"
---
# <a name="attribute_record_header-structure"></a>屬性 \_ 記錄 \_ 標頭結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

表示屬性記錄。

## <a name="syntax"></a>語法


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**TypeCode**
</dt> <dd>

屬性型別程式碼。



| 值                                                                                                                                                                                                                                           | 意義                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_資訊**</dt> <dt>0x10</dt> </dl> | 檔案屬性 (例如唯讀和封存) 、時間戳記 (例如檔案建立和上次修改的) ，以及固定連結計數。<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_列出**</dt> <dt>0x20</dt> </dl>                   | 組成檔案的屬性清單，以及每個屬性所在之 MFT 檔案記錄的檔案參考。<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_名稱**</dt> <dt>0x30<</dt> </dl>                                  | 檔案名（以 Unicode 字元為單位）。<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_識別碼**</dt> <dt>0x40</dt> </dl>                                  | 連結追蹤服務所指派的64位元組物件識別碼。<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_名稱**</dt> <dt>0x60</dt> </dl>                            | 磁碟區標籤。 存在於 $Volume 檔案中。<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_資訊**</dt> <dt>0x70</dt> </dl>       | 磁片區資訊。 存在於 $Volume 檔案中。<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | 檔案的內容。<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_根**</dt> <dt>0x90</dt> </dl>                               | 用來執行大型目錄的檔案名配置。<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_配置**</dt> <dt>0xA0</dt> </dl>             | 用來執行大型目錄的檔案名配置。<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | 大型目錄的點陣圖索引。<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_點**</dt> <dt>0xC0</dt> </dl>                      | 重新分析點資料。<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

屬性記錄的大小（以位元組為單位）。 此值會反映記錄變異所需的大小，且一律會四捨五入為最接近的四乘條界限。

</dd> <dt>

**FormCode**
</dt> <dd>

屬性表單程式碼。



| 值                                                                                                                                                                                                                            | 意義                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**常駐 \_格式**</dt> <dt>0x00</dt> </dl>          | 值會包含在檔案記錄中，並緊接在屬性記錄標頭之後。<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <dt>**NONRESIDENT \_表單**</dt> <dt>0x01</dt> </dl> | 此值會包含在磁片上的其他磁區中。<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

選擇性屬性名稱的大小（以字元為單位），如果沒有屬性名稱，則為0。 最大屬性名稱長度為255個字元。

</dd> <dt>

**NameOffset**
</dt> <dd>

屬性名稱從屬性記錄開頭算起的位移（以位元組為單位）。 如果 **NameLength** 成員為0，則這個成員是未定義的。

</dd> <dt>

**旗標**
</dt> <dd>

屬性旗標。

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**屬性 \_旗標 \_ 壓縮 \_ 遮罩** (0x00FF) 
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**屬性 \_標記 \_ 稀疏** (0x8000) 
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**屬性 \_旗 \_** 標已加密 (0x4000) 
</dt> </dl> </dd> <dt>

**執行個體**
</dt> <dd>

檔案記錄中這個屬性的唯一實例。

</dd> <dt>

**表單**
</dt> <dd>

如果 **FormCode** 成員是常駐 \_ 表單，則聯集是 **常駐** 結構。 如果 **FormCode** 是 NONRESIDENT \_ 格式，則聯集是 **NONRESIDENT** 結構。

<dl> <dt>

**居民**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

屬性值的大小（以位元組為單位）。

</dd> <dt>

**ValueOffset**
</dt> <dd>

從屬性記錄開頭算起的值位移（以位元組為單位）。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> </dl> </dd> <dt>

**Nonresident**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

此屬性記錄所涵蓋 (VCN) 的最低虛擬叢集編號。

</dd> <dt>

**HighestVcn**
</dt> <dd>

這個屬性記錄所涵蓋的最高 VCN。

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

從屬性記錄開頭開始對應組陣列的位移，以位元組為單位。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**AllocatedLength**
</dt> <dd>

設定檔案大小（以位元組為單位）。 此值是叢集大小的偶數倍數。 如果 **LowestVcn** 成員為非零，則這個成員是不正確。

</dd> <dt>

**FileSize**
</dt> <dd>

檔案大小 (可讀取的最大位元組加 1) （以位元組為單位）。 如果 **LowestVcn** 為非零值，則此成員無效。

</dd> <dt>

**ValidDataLength**
</dt> <dd>

有效的資料長度 (最高初始化的位元組加 1) （以位元組為單位）。 此值會舍入到最接近的叢集界限。 如果 **LowestVcn** 為非零值，則此成員無效。

</dd> <dt>

**TotalAllocated**
</dt> <dd>

配置給檔案的總計 (配置的叢集) 的總和。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

請注意，此結構沒有相關聯的標頭檔。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

屬性記錄一律會在四個四個線界限上對齊。

如果屬性為 nonresident，屬性記錄標頭會包含抓取資訊的清單，這些資訊會在屬性的 (LCN) 的 VCN 和邏輯群集編號之間提供對應。 如果起始資訊無法放入基底檔案區段中，則可以將它本身儲存在外部檔案記錄區段中。 如果它仍無法放入一個外部檔案記錄區段中，屬性清單中會有一個布建，可針對需要額外抓取資訊的屬性包含多個專案。

對應配對陣列是以壓縮格式儲存，並假設系統會將資訊解壓縮和快取。 它是由一系列的 NextVcn/CurrentLcn 配對所組成。 例如，如果檔案的單一執行8個叢集從 LCN 128 開始，且檔案從 LowestVcn 0 開始，則對應組陣列只會有一個專案，也就是 NextVcn = 8 和 CurrentLcn = 128。 陣列是位元組串流，會在依序處理時儲存工作變數的變更。 位元組資料流程會被視為以零結束的三合一資料流程，如下所示：

count byte = *v* + (*l* \* 16) 

其中 *v* 是變更低順序的 VCN 位元組數目，而 *l* 是變更的低順序的 LCN 位元組數目。

解壓縮演算法如下所示：

1.  將 NextVcn 初始化為 `Attribute->LowestVcn` ，並將 CurrentLcn 設為0。
2.  初始化的位元組資料流程指標 `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` 。
3.  將 CurrentVcn 設定為 NextVcn。
4.  讀取資料流程中的下一個位元組。 如果是0，則中斷;否則如先前所述，請將 *v* 和 *l* 解壓縮。
5.  將下一個 *v* 位元組解讀為帶正負號的數量（低序位位元組優先）。 將其簽章解壓縮至64位並將它新增至 NextVcn。
6.  將下一個 *l* 位元組解讀為帶正負號的數量（低序位位元組優先）。 將其簽章解壓縮至64位並將它新增至 CurrentLcn。 如果這產生的 CurrentLcn 為0，則從 CurrentVcn 到 NextVcn-1 的 VCNs 尚未配置。
7.  從 CurrentVcn、NextVcn 和 CurrentLcn 更新快取的對應資訊。
8.  移至步驟 3。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
