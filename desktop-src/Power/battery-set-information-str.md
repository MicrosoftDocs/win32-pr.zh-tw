---
description: 包含要設定的電池資訊。
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: 'BATTERY_SET_INFORMATION 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c53e9c539f8ef20b184c6c056999c7c541f3c1718bafaa58c0b1e20dcef16a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143611"
---
# <a name="battery_set_information-structure"></a>電池 \_ 設定 \_ 資訊結構

包含要設定的電池資訊。 此結構會與 [**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md) 控制程式代碼搭配使用。

## <a name="syntax"></a>語法


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**BatteryTag**
</dt> <dd>

電池目前的電池標記。 只會傳回符合標記之電池的資訊。 每當此值不符合電池的目前標記時，就會完成 IOCTL 要求，並找不到錯誤檔案 \_ \_ \_ ，這會向呼叫者指出其具有標記的電池已不存在。 呼叫者可以選擇使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業來判斷新安裝的電池標記（如果有的話）。  (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) 

發出查詢資訊要求時，會驗證此值。 此外，如果此值變更時，要求仍在進行中，則會中止要求，並出現「找不到錯誤檔案」的狀態 \_ \_ \_ 。

</dd> <dt>

**InformationLevel**
</dt> <dd>

要設定的電池資訊。 **緩衝區** 成員中的資料類型取決於這個成員的值。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | 通知電池裝置，表示使用者已要求電池必須在這段時間充電。 例如，使用智慧型電池/充電器/選擇器時，應用程式可以一次收取一台電池的費用。 忽略此結構的 **緩衝區** 成員。<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | 設定電池的重大偏差調整。 請注意，此值通常會由軟體變更，而且只會在介面中顯示為維護功能。 並非所有電池都可以維持這種設定，而且應該閱讀電池資訊，以確認電池已接受設定。<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | 通知電池裝置，使用者目前已要求電池即將放電。 例如，這可以用來指出使用者目前要為系統提供哪些電池電力。 忽略此結構的 **緩衝區** 成員。<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

要設定的電池資訊。 資料取決於 **InformationLevel** 的值。

</dd> </dl>

## <a name="remarks"></a>備註

**電池 \_ 設定 \_ 資訊** 結構是可變長度的結構，而且您必須配置適當大小的緩衝區，才能將資訊包含在結構中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 Batclass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




