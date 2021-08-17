---
description: 包含處理器的相關資訊。
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3bdb6a3bb8ae5b768c42609817c76934c203989ba6dea665fc6cc0a6896659de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143331"
---
# <a name="processor_power_information-structure"></a>處理器 \_ 電源 \_ 資訊結構

包含處理器的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**Number**
</dt> <dd>

系統處理器號碼。

</dd> <dt>

**MaxMhz**
</dt> <dd>

系統處理器指定的最大頻率（以 mhz 為單位）。

</dd> <dt>

**CurrentMhz**
</dt> <dd>

處理器時鐘頻率（以 mhz 為單位）。 此數位是指定的處理器頻率頻率上限乘以目前的處理器節流。

</dd> <dt>

**MhzLimit**
</dt> <dd>

處理器時鐘頻率的限制（以 mhz 為單位）。 此數位是指定的處理器頻率頻率上限乘以目前的處理器熱節流限制。

</dd> <dt>

**MaxIdleState**
</dt> <dd>

此處理器的最大閒置狀態。

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

此處理器的目前空閒狀態。

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

 

 




