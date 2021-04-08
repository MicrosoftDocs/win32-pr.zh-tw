---
title: 'PROTOCOL_SPECIFIC_DATA 結構 (Rtm) '
description: 通訊協定 \_ 特定的 \_ 資料結構包含特定路由通訊協定專屬資料的保留記憶體。
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA 結構 RAS
- PPROTOCOL_SPECIFIC_DATA 結構指標 RAS
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686080"
---
# <a name="protocol_specific_data-structure"></a>通訊協定 \_ 特定的 \_ 資料結構

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**通訊協定 \_ 特定的 \_ 資料** 結構包含特定路由通訊協定專屬資料的保留記憶體。

## <a name="syntax"></a>語法


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**PSD \_ 資料**
</dt> <dd>

指定 **DWORD** 變數的陣列。 此記憶體會保留給路由通訊協定專用的資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Rtm. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[路由表管理員第1版參考](routing-table-manager-version-1-reference.md)
</dt> <dt>

[路由表管理員第1版結構](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ 路由**](rtm-ipx-route.md)
</dt> </dl>

 

 





