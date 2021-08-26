---
description: 包含電池製造日期。
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: 'BATTERY_MANUFACTURE_DATE 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 30a70fed151304d189fa91b20106e1154ca0e9f4ea5225c52bf1023dbd218346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032968"
---
# <a name="battery_manufacture_date-structure"></a>電池 \_ 製造 \_ 日期結構

包含電池製造日期。 要求 BatteryManufactureDate 資訊層級時， [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md) 結構會使用此結構。

## <a name="syntax"></a>語法


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>成員

<dl> <dt>

**Day**
</dt> <dd>

製造月份的第一天，範圍介於1到31之間。 儘管是資料類型，但這不是 ASCII 編碼值。 它是不帶正負號的位元組。

</dd> <dt>

**月**
</dt> <dd>

製造的月份，範圍 1 (1 月) 至 12 (12 月) 。 儘管是資料類型，但這不是 ASCII 編碼值。 它是不帶正負號的位元組。

</dd> <dt>

**Year**
</dt> <dd>

製造的年份。 這通常會在1900-2100 範圍內。

</dd> </dl>

## <a name="remarks"></a>備註

日期是以西曆或西方日曆格式編碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 Batclass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




