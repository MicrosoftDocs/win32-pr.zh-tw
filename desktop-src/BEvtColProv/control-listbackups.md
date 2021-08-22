---
description: 傳回可以還原的已儲存備份配置檔案清單。
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Control 類別的 ListBackups 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ba6a3f042a6bd8f01e4bede00e22bda95ca28ebe7cc2beb33a12c6b49deba6bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589118"
---
# <a name="listbackups-method-of-the-control-class"></a>Control 類別的 ListBackups 方法

傳回可以還原的已儲存備份配置檔案清單。

## <a name="syntax"></a>語法


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OriginalTimestampLow* \[擴展\]
</dt> <dd>

目前設定的設定時間戳記 (如果從備份還原，將會包含原始的時間戳記) 。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。

</dd> <dt>

*OriginalTimestampHigh* \[擴展\]
</dt> <dd>

目前設定的設定時間戳記 (如果從備份還原，將會包含原始的時間戳記) 。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。

</dd> <dt>

檔案 \[擴展\]
</dt> <dd>

可用備份檔案的清單，順序從最新到最舊。

</dd> <dt>

*FilesTimestampLow* \[擴展\]
</dt> <dd>

針對每個備份檔案，設定其設定的時間戳記。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。

</dd> <dt>

*FilesTimestampHigh* \[擴展\]
</dt> <dd>

針對每個備份檔案，設定其設定的時間戳記。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control.md)
</dt> </dl>

 

