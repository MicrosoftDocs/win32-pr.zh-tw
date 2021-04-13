---
title: CHANGE_LOG_HEADER 結構
description: 變更記錄標頭。
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- CHANGE_LOG_HEADER 結構系統還原
- PCHANGE_LOG_HEADER 結構指標系統還原
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383994"
---
# <a name="change_log_header-structure"></a>變更 \_ 記錄 \_ 標頭結構

\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]

變更記錄標頭。

## <a name="syntax"></a>語法


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**RecordHeader**
</dt> <dd>

[**記錄 \_ 標頭**](record-header.md)結構。 **DwRecordType** 成員應設定為 RecordTypeLogHeader (0) 。 **DwRecordSize** 成員應考慮所有成員，再加上此標頭後面的額外 **DWORD** 值。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**dwMagicNum**
</dt> <dd>

此成員應設定為0xabcdef12。

</dd> <dt>

**dwLogVersion**
</dt> <dd>

此成員應設定為2。

</dd> <dt>

**DataHeader**
</dt> <dd>

[**記錄 \_ 標頭**](record-header.md)結構。 **DwRecordType** 成員應設定為 **RecordTypeVolumePath** (2) 。

</dd> <dt>

**byteData**
</dt> <dd>

指定磁片區路徑之以 null 結束的字串開頭。

</dd> </dl>

## <a name="remarks"></a>備註

此標頭後面接著應與 **RecordHeader** 的 **dwRecordSize** 成員值相同的 **DWORD** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                            |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                       |



 

 





