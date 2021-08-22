---
description: 包含系統之空閒的相關資訊。
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: SYSTEM_POWER_INFORMATION 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 665c19a99bffae46cf20af8c5c634e2e9594ecd07d02f003f56d42277ce9a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143301"
---
# <a name="system_power_information-structure"></a>系統 \_ 電源 \_ 資訊結構

包含系統之空閒的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**MaxIdlenessAllowed**
</dt> <dd>

系統被視為閒置且空閒超時時間開始計數的閒置時間，以百分比表示。 放在此數位下面會導致計時器取消。

</dd> <dt>

**閒置**
</dt> <dd>

目前的閒置層級，以百分比表示。

</dd> <dt>

**TimeRemaining**
</dt> <dd>

閒置計時器的剩餘時間（以秒為單位）。

</dd> <dt>

**CoolingMode**
</dt> <dd>

目前的系統冷卻模式。 此成員必須是下列值之一。



| 值                                                                                                                                                                                                                                 | 意義                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**PO \_TZ \_ 活動**</dt> <dt>0</dt> </dl>                    | 系統目前處於主動冷卻模式。<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**PO \_TZ \_ 無效 \_ 模式**</dt> <dt>2</dt> </dl> | 系統不支援 CPU 節流，或系統中未定義任何熱區域。<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**PO \_TZ \_ 被動**</dt> <dt>1</dt> </dl>                 | 系統目前處於被動冷卻模式。<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>備註

請注意，在 WinNT 中不小心省略此結構定義。 此錯誤會在未來修正。 在此同時，若要編譯您的應用程式，請將本主題中所包含的結構定義包含在原始程式碼中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




