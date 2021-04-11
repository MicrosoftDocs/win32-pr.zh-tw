---
description: 表示檔案名屬性。 針對輸入的每個目錄，檔案都有一個檔案名屬性。
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: FILE_NAME 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025817"
---
# <a name="file_name-structure"></a>檔案名 \_ 結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

表示檔案名屬性。 針對輸入的每個目錄，檔案都有一個檔案名屬性。

## <a name="syntax"></a>語法


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>成員

<dl> <dt>

**ParentDirectory**
</dt> <dd>

針對此名稱編制索引之目錄的檔案參考。 請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**FileNameLength**
</dt> <dd>

檔案名的長度（以 Unicode 字元為單位）。

</dd> <dt>

**旗標**
</dt> <dd>

檔案名旗標。

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**檔案 \_名稱 \_ NTFS** (0x01) 
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**檔案 \_名稱 \_ DOS** (0x02) 
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

檔案名的第一個字元。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，此結構沒有相關聯的標頭檔。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
