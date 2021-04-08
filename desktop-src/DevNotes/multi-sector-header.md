---
description: 表示 multisector 標頭。
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688619"
---
# <a name="multi_sector_header-structure"></a>多 \_ 磁區 \_ 標頭結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

表示 multisector 標頭。

## <a name="syntax"></a>語法


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**簽名**
</dt> <dd>

簽章。 此值是使用者的便利性。

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

更新順序陣列的位移，從這個結構的開頭算起。 更新順序陣列必須在第一個磁區的最後一個 USHORT 值之前結束。

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

更新順序陣列的大小（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，此結構沒有相關聯的標頭檔。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

Multisector 標頭和更新順序陣列針對實體磁區大小大於或等於序號 stride (512) 或未依順序傳送磁區的裝置，提供不完整的 multisector 傳輸偵測。 如果有磁區大小小於序號 stride 的裝置，而且有時會依序傳送磁區，則更新序列陣列將不會提供不完整傳輸的絕對偵測。 序號 stride 設定為夠小的數位，以提供所有已知硬碟的絕對保護。 它未設定為較小，或可能有過多的執行時間或空間額外負荷。

更新順序陣列包含 *n* **USHORT** 值的陣列，其中 *n* 是受保護的結構大小除以序號 stride。 第一個單字包含更新序號，也就是包含結構寫入磁片的次數的迴圈計數器。 接下來是在最後一次將包含結構寫入磁片時，更新序號所覆寫的 *n* 個儲存的 **USHORT** 值。

每次受保護的結構即將寫入磁片時，每個序號 stride 中的最後一個單字會儲存至序號陣列中的個別位置，然後以下一個更新序號加以覆寫。 在寫入之後，或每次讀取結構時，序號陣列中儲存的單字會還原為其在結構中的實際位置。 在讀取上儲存的文字之前，每個 stride 結尾的所有序號都會與陣列開頭的實際序號進行比較。 如果其中任何一項比較不相等，則會偵測到失敗的 multisector 轉移。

陣列的大小取決於包含結構的大小。 更新順序陣列應包含在它所保護之結構的標頭結尾，因為它的變數大小。 使用者必須確定為包含結構保留正確的空間：結構/512 + 1) \* sizeof (USHORT) 的 (大小。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
