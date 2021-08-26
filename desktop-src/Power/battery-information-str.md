---
description: 包含電池資訊。
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: 'BATTERY_INFORMATION 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c449f325e03fb4ea81fe0aa148eaddcf65800b5a56356e22232477e0b6d4fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033008"
---
# <a name="battery_information-structure"></a>電池 \_ 資訊結構

包含電池資訊。 當要求 BatteryInformation 資訊層級時，[ [**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md) ] 控制項程式碼會傳回這個結構。

## <a name="syntax"></a>語法


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**Capabilities**
</dt> <dd>

電池功能。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                                                                                 | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**電池 \_容量 \_ 相對**</dt> <dt>0x40000000</dt> </dl>                    | 指出電池容量和費率資訊是相對的，而不是任何特定的單位。 如果未設定此位，報表單位會是毫瓦時數 (mWh) 的容量和毫瓦 (mW) 的費率。 如果設定此位，則可以忽略其他電池檔中的所有單位參考。 所有費率資訊都會以每小時的單位回報。 例如，如果將完全收費的容量回報為100，則速率為200，表示電池將會在半小時內使用其所有容量。<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**電池 \_是 \_ 短期 \_**</dt> <dt>0x20000000</dt> </dl>                               | 表示正常作業適用于不安全的函式。 如果未設定此位，則應該在正常系統使用期間使用電池。<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**電池 \_設定 \_ \_ 支援的費用**</dt> <dt>0x00000001</dt> </dl>          | 指出此電池裝置支援 BatteryCharge 類型的設定資訊要求。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**電池 \_設定 \_ 放電 \_ 支援**</dt> <dt>0x00000002</dt> </dl> | 指出此電池裝置支援 BatteryDischarge 類型的設定資訊要求。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**電池 \_系統 \_ 電池**</dt>的 <dt>0x80000000</dt> </dl>                             | 指出電池可提供一般電源來執行系統。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**技術**
</dt> <dd>

電池技術。 這個成員可以是下列其中一個值。



| 值                                                                        | 意義                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nonrechargeable 電池，例如，鹼性。<br/> |
| <dl> <dt>1</dt> </dl> | 充電電池，例如潛在客戶 acid。<br/>   |



 

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**化學**
</dt> <dd>

表示電池化學的縮寫字元字串。 這個字串不一定是以零結束。 以下是可傳回的縮寫部分清單，以及相關聯的 chemistries。



| Unicode 字串                                                                                                                                           | 意義                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | 潛在客戶 Acid<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**獅子**</dt> </dl>                        | 鋰離子<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li**</dt> </dl> | 鋰離子<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**NiCd**</dt> </dl> | 五分錢鎘<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**Nimh**</dt> </dl> | 五分錢金屬氫化<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | 五分錢 Zinc<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | 充電 Alkaline-Manganese<br/> |



 

未來可能會出現其他 chemistries，且您的程式碼應該能夠處理它們。

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

在 mWh 時的最新電池容量，除非 \_ 已設定電池容量 \_ 相對。 在此情況下，單位是未定義的。

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

MWh (或相對) 中電池的目前完全收費容量。 比較此值與 **DesignedCapacity** ，以預估電池的損耗。

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

製造商的建議容量（以 mWh），也就是電力偏低的警示。 [低] 的定義會因製造商而異。 一般情況下，會在低狀態之前發生警告狀態，但您不應該假設它一律會發生。 為了降低資料遺失的風險，通常會使用此值做為重大電池警示的預設設定。

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

製造商的建議容量（以 mWh），此時會出現警告電池警示。 警告的定義會因製造商而異。 一般情況下，會在低狀態之前發生警告狀態，但您不應該假設它一律會發生。 為了降低資料遺失的風險，通常會使用此值做為低電池警示的預設設定。

</dd> <dt>

**CriticalBias**
</dt> <dd>

從零到 mWh 的偏差，這會套用到電池報告。 某些電池會保留一小部分，並將電池的容量值偏低，以將 "0" 顯示為電力偏高等級。 重大偏差類似于設定燃料量測計，以在有數個偏升的燃料時顯示「空白」。

</dd> <dt>

**CycleCount**
</dt> <dd>

電池所經歷的收費/放電週期數。 這提供了一種方法來判斷電池磨損。 如果電池不支援迴圈計數器，此成員為零。

</dd> </dl>

## <a name="remarks"></a>備註

警告狀態通常會在低狀態之前發生，但您不應該假設它將會。 您可以輪詢電池並找出未發生警示等級，然後再次輪詢電池，並找出這兩個層級達到的程度。 這可能表示您的輪詢頻率不足。 這也可能表示電池無法維持很長的費用，而且正在進行比預期更快的放電。 這類電池可能會接近其使用年限的結尾，或可能已損毀。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 Batclass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




