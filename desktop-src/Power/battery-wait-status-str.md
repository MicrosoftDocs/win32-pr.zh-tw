---
description: 包含要取出電池狀態的條件相關資訊。
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: 'BATTERY_WAIT_STATUS 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996734"
---
# <a name="battery_wait_status-structure"></a>電池 \_ 等待 \_ 狀態結構

包含要取出電池狀態的條件相關資訊。 此結構是由 [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md) 控制程式代碼使用。

## <a name="syntax"></a>語法


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**BatteryTag**
</dt> <dd>

電池目前的電池標記。 只會傳回符合標記之電池的資訊。 每當此值與電池的目前標籤不相符時， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 作業將會失敗，並出現錯誤檔案的錯誤碼 \_ \_ \_ ，這會向呼叫者指出其具有標記的電池已不再安裝，呼叫者可能會選擇使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業來判斷新安裝電池的標記（如果有的話）。 此外，如果在移除電池或標記變更時要求正在進行中，則作業會中止，並出現 [ \_ \_ 找不到錯誤檔案] 的狀態 \_ 。  (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) 

</dd> <dt>

**逾時**
</dt> <dd>

在完成之前，要求會等待 **>powerstate**、 **LowCapacity** 和 **HighCapacity** 成員所指定之條件的毫秒數。 值為-1 表示要求將會無限期等候，以滿足條件。 值為零表示要求的電池資訊會立即傳回，而不考慮其他狀況。 任何其他值則表示要求應該等候該時間長度，或直到滿足任何其他條件為止。

如果電腦進入睡眠模式，時鐘將會繼續執行，但耗盡計數不會喚醒電腦。 如果在電腦喚醒時，計數會耗盡，且符合其他條件，則呼叫會立即在喚醒上傳回。

</dd> <dt>

**>powerstate**
</dt> <dd>

零、一或多個下列狀態位，表示電池的狀態。 它等同于 [**電池 \_ 狀態**](battery-status-str.md)結構的 **>powerstate** 成員。



| 值                                                                                                                                                                                                                                                   | 意義                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**電池 \_充電**</dt> <dt>0x00000004</dt> </dl>                  | 指出電池目前正在充電。<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**電池 \_重大**</dt> <dt>0x00000008</dt> </dl>                  | 指出電池故障即將發生。 如需詳細資訊，請參閱＜備註＞一節。<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**電池 \_放電**</dt> <dt>0x00000002</dt> </dl>         | 指出電池目前正在進行放電。<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**電池 \_\_第 0x00000001 \_ 行電源**</dt> <dt></dt> </dl> | 指出電池可存取 AC 電源。<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

目前的電池容量，以 mWh (或相對) 。 此值與 [**電池 \_ 狀態**](battery-status-str.md)結構的 **容量** 成員相同。

</dd> <dt>

**HighCapacity**
</dt> <dd>

目前的電池容量，以 mWh (或相對) 。 此值與 [**電池 \_ 狀態**](battery-status-str.md)結構的 **容量** 成員相同。

</dd> </dl>

## <a name="remarks"></a>備註

電池資訊的要求會延後，直到發生下列其中一種情況為止：

-   超時時間過期 (假設 **Timeout** 不是-1) 。
-   電池的目前狀態與 **>powerstate** 不符。
-   電池容量低於 **LowCapacity**。
-   電池容量高於 **HighCapacity**。
-   電池標記變更。

當符合上述任一條件時，便會收集資料，而作業會傳回。 這可讓應用程式監視一般動態電池資訊，而不需輪詢裝置。

使用兩種容量條件的其中之一之前，請使用 [ [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md) ] 控制項程式碼，並以零為限時，確定電池支援它們。 檢查結果，以判斷是否支援 **容量** 成員， (也就是，不是電池 \_ 未知 \_ 容量) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電池 \_ 狀態**](battery-status-str.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md)
</dt> </dl>

 

