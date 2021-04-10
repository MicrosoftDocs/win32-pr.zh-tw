---
description: 表示屬性清單中的專案。
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847016"
---
# <a name="attribute_list_entry-structure"></a>屬性 \_ 清單 \_ 專案結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

表示屬性清單中的專案。

## <a name="syntax"></a>語法


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**AttributeTypeCode**
</dt> <dd>

屬性型別程式碼。



| 值                                                                                                                                                                                                                                           | 意義                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_資訊**</dt> <dt>0x10</dt> </dl> | 檔案屬性 (例如唯讀和封存) 、時間戳記 (例如檔案建立和上次修改的) ，以及固定連結計數。<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_列出**</dt> <dt>0x20</dt> </dl>                   | 組成檔案的屬性清單，以及每個屬性所在之 MFT 檔案記錄的檔案參考。<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_名稱**</dt> <dt>0x30<</dt> </dl>                                  | 檔案名（以 Unicode 字元為單位）。<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_識別碼**</dt> <dt>0x40</dt> </dl>                                  | 連結追蹤服務所指派的16位元組物件識別碼。<br/>                                                              |
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

此結構的大小，加上選擇性的名稱緩衝區（以位元組為單位）。

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

選用屬性名稱的大小（以字元為單位）。 如果名稱存在，此值為非零值，且結構後面緊接著指定字元數的 Unicode 字串。

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

保留的。

</dd> <dt>

**LowestVcn**
</dt> <dd>

此屬性 (VCN) 的最低虛擬叢集編號。 除非屬性需要多個檔案記錄區段，而且這個專案是第一個區段的參考，否則這個成員是零。 在此情況下，此值是參考區段所描述的最小 VCN。

</dd> <dt>

**SegmentReference**
</dt> <dd>

主要檔案資料表 (屬性所在的 MFT) 區段。 請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**AttributeName**
</dt> <dd>

選擇性屬性名稱的開頭。

</dd> </dl>

## <a name="remarks"></a>備註

[屬性] 清單是以雙線對齊的 **屬性 \_ 清單 \_ 專案** 結構的排序清單。 這份清單會先依屬性類型代碼排序，然後依屬性名稱 (（如果有) ）。 兩個屬性都不能有相同的類型代碼、名稱和最低的 VCN。 因此，每個類型的程式碼最多隻能有一個屬性，沒有名稱。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

請注意，此結構沒有相關聯的標頭檔。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
