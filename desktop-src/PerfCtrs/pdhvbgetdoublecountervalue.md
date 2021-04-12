---
description: PdhVbGetDoubleCounterValue 函式會將指定計數器的目前值傳回為雙精確度浮點值。
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319180"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>PdhVbGetDoubleCounterValue 函式

**PdhVbGetDoubleCounterValue** 函式會將指定計數器的目前值傳回為雙精確度浮點值。 使用傳回的數位之前，您應該先檢查 *CounterStatus* ，因為計數器在讀取時可能無效。 若要檢查計數器狀態，請呼叫 [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) 函數。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函式 PdhVbGetDoubleCounterValue ( \_ Byval CounterHandle long， \_ Byval CounterStatus 的 Long \_ ) 為 Double

## <a name="parameters"></a>參數

<dl> <dt>

*CounterHandle* 
</dt> <dd>

要讀取其目前值之計數器的識別碼。

</dd> <dt>

*CounterStatus* 
</dt> <dd>

變數，其中計數器值的目前狀態會傳回給呼叫者。 只有在 CounterStatus 中傳回的值為 PDH \_ CSTATUS 有效資料或 pdh CSTATUS 新資料時，傳回的資料值才有效， \_ \_ \_ \_ \_ (查看 pdh 錯誤碼) 。 如果 CounterStatus 中所傳回的值是任何其他值，請勿使用資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回目前計數器的雙精確度浮點值（依計數器類型的定義計算和格式化）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




