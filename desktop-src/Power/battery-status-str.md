---
description: 包含電池的目前狀態。
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: 'BATTERY_STATUS 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 28b75a8eb1c7abf647f3f8ea61b29dedb40978f3ea639fc505364a12ae5e57cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143601"
---
# <a name="battery_status-structure"></a>電池 \_ 狀態結構

包含電池的目前狀態。 此結構是由 [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md) 控制程式代碼使用。

## <a name="syntax"></a>語法


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**>powerstate**
</dt> <dd>

電池狀態。 這個成員可以是零、一或多個下列值。



| 值                                                                                                                                                                                                                                                   | 意義                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**電池 \_充電**</dt> <dt>0x00000004</dt> </dl>                  | 指出電池目前正在充電。<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**電池 \_重大**</dt> <dt>0x00000008</dt> </dl>                  | 指出電池故障即將發生。 如需詳細資訊，請參閱＜備註＞一節。<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**電池 \_放電**</dt> <dt>0x00000002</dt> </dl>         | 指出電池目前正在進行放電。<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**電池 \_\_第 0x00000001 \_ 行電源**</dt> <dt></dt> </dl> | 指出系統可存取 AC 電源，因此沒有電池正在進行放電。<br/>   |



 

</dd> <dt>

**容量**
</dt> <dd>

目前的電池容量，以 mWh (或相對) 。 此值可透過 **FullChargedCapacity** [**電池 \_ 資訊**](battery-information-str.md) 結構的成員除以，來產生「天然氣量測計」顯示。 如果容量無法使用，此成員會是電池 \_ 未知的 \_ 容量。

</dd> <dt>

**電壓**
</dt> <dd>

電池端子的目前電池電壓，以毫伏 (mv) 。 如果無法使用電壓，此成員會是電池 \_ 未知 \_ 電壓。

</dd> <dt>

**速率**
</dt> <dd>

目前的電池計量或放電的速率。 此值將會在毫瓦中，除非電池速率資訊是相對的，在此情況下，它將會以任意單位每小時為單位。 若要判斷電池資訊是否為相對，請檢查 \_ \_ [**電池 \_ 資訊**](battery-information-str.md)結構的 **功能** 成員中的電池容量相對旗標。 非零的正面比率表示充電;負的速率表示已放電。 某些電池只會報告放電費率。 如果無法使用速率，此成員會是電池 \_ 未知 \_ 費率。 如果電池或電源來源的狀態變更，速率可能會變成可用。

</dd> </dl>

## <a name="remarks"></a>備註

\_此結構之 **>powerstate** 成員中的電池關鍵性旗標表示硬體「電池關鍵性」條件。 這個關鍵層級是由電池製造商設定，而不是由使用者在「電力嚴重不足警示」中設定。 這通常表示電池系統已計算出電池已完全耗盡，而任何正在繪製的電源超出預期。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 Batclass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電池 \_ 資訊**](battery-information-str.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




