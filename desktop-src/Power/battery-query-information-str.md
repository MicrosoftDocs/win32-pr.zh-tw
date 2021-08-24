---
description: 包含電池查詢資訊。
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: 'BATTERY_QUERY_INFORMATION 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 9049517108cbb31df1164cc88640a78e104e2902d3a8a4b8dec4b8bfb48e8a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143681"
---
# <a name="battery_query_information-structure"></a>電池 \_ 查詢 \_ 資訊結構

包含電池查詢資訊。 此結構會與 [**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md) 控制項程式碼搭配使用，以指定要傳回的資訊類型。

## <a name="syntax"></a>語法


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**BatteryTag**
</dt> <dd>

電池目前的電池標記。 只會傳回符合標記之電池的資訊。 每當此值不符合電池的目前標記時，就會完成 IOCTL 要求，並 \_ \_ 找不到錯誤檔案 \_ 。 這會向呼叫者指出與標記相關聯的電池已存在。 呼叫者可以選擇使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業來判斷新安裝的電池標記（如果有的話）。  (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) 

發出查詢資訊要求時，會驗證此值。 此外，如果此值變更時，要求仍在進行中，則會中止要求，並出現「找不到錯誤檔案」的狀態 \_ \_ \_ 。

</dd> <dt>

**InformationLevel**
</dt> <dd>

正在查詢的電池資訊層級。 由 IOCTL 傳回的資料取決於此值。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | 以 Null 終止的 Unicode 字串，其中包含電池的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | 指定預估電池執行時間（以秒為單位）的 **ULONG** 。 如果 **電池 \_ 查詢 \_ 資訊** 結構的 **AtRate** 成員中提供的清空率為零，則此計算是以目前的清空率為基礎。 如果 **AtRate** 為非零值，則傳回的時間會是指定速率的預期執行時間。 如果預估的時間不明 (例如，電池未放電，且指定的 **AtRate** 為零) ，則傳回值為電池 \_ 未知 \_ 時間。 請注意，在某些電池系統上，此值不太精確，而且可能會因為目前的電源使用量而異，可能會受到磁片活動和其他因素所影響。 此值的變更不會有任何通知機制。<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | [**電池 \_ 報告 \_ 規模**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)結構的陣列，不超過四個專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | [**電池 \_ 資訊**](battery-information-str.md)結構。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | [**電池 \_ 製造 \_ 日期**](battery-manufacture-date-str.md)結構。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | 以 Null 結束的 Unicode 字串，指定電池的製造商名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | 以 Null 結束的 Unicode 字串，指定電池的序號。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | 指定電池目前溫度的 **ULONG** ，以10ths 角度的角度。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | 以 Null 結束的 Unicode 字串，可唯一識別電池。 這個值可以用來追蹤特定電池。 在智慧電池的情況下，此識別碼會是製造商名稱、裝置名稱、製造日期，以及序號可列印標記法的串連。 <br/> 此值不適合顯示給使用者。<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

只有在 **InformationLevel** 為 BatteryEstimatedTime 時，才會使用這個成員。

如果這個成員為非零值，則會用來計算時間，直到電池放電以 BatteryEstimatedTime 個別電池的速率。 它必須在 mW 中指定，而且必須是負數值，以代表電池放電率。

</dd> </dl>

## <a name="remarks"></a>備註

某些電池的相關資訊是選擇性的，或可能對某些電池沒有意義。 如果目前的電池無法使用所要求的特定資料類型，則會傳回錯誤不正確函式 \_ \_ 。

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

[**電池 \_ 製造 \_ 日期**](battery-manufacture-date-str.md)
</dt> <dt>

[**電池 \_ 報告 \_ 規模**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




