---
description: 包含 [active File Manager] 視窗中所選磁片磁碟機的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。
title: 'FMS_GETDRIVEINFO 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973221"
---
# <a name="fms_getdriveinfo-structure"></a>FMS \_ GETDRIVEINFO 結構

包含 [active File Manager] 視窗中所選磁片磁碟機的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。

## <a name="syntax"></a>語法


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

磁片磁碟機相關磁片的總儲存空間量（以位元組為單位）。

</dd> <dt>

**dwFreeSpace**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

磁片磁碟機相關磁片的可用儲存空間量（以位元組為單位）。

</dd> <dt>

**szPath**
</dt> <dd>

類型： **TCHAR \[ 260 \]**

</dd> <dd>

目前的目錄的以 null 結束路徑。

</dd> <dt>

**szVolume**
</dt> <dd>

類型： **TCHAR \[ 14 \]**

</dd> <dd>

與磁片磁碟機相關聯之磁片的以 null 終止的磁片區標籤。

</dd> <dt>

**szShare**
</dt> <dd>

類型： **TCHAR \[ 128 \]**

</dd> <dd>

如果透過網路) 存取磁片磁碟機，則為網路資源 (以 null 終止的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETDRIVEINFO**](fm-getdriveinfo.md)
</dt> </dl>

 

 




