---
description: 包含標準資訊屬性。 這個屬性存在於每個基底檔案記錄中，而且必須是常駐的。
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: STANDARD_INFORMATION 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025809"
---
# <a name="standard_information-structure"></a>標準 \_ 資訊結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

包含標準資訊屬性。 這個屬性存在於每個基底檔案記錄中，而且必須是常駐的。

## <a name="syntax"></a>語法


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**OwnerId**
</dt> <dd>

來自安全性索引的檔案擁有者識別碼。

</dd> <dt>

**SecurityId**
</dt> <dd>

檔案的安全識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，此結構沒有相關聯的標頭檔。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
