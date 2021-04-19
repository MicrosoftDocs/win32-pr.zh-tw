---
description: PdhVbIsGoodStatus 函式會測試狀態值，以判斷其是否為成功或失敗的程式碼。 如果狀態值為成功，則傳回值將為非零值。 如果這是失敗狀態碼，傳回值將會是零。
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986938"
---
# <a name="pdhvbisgoodstatus-function"></a>PdhVbIsGoodStatus 函式

**PdhVbIsGoodStatus** 函式會測試狀態值，以判斷其是否為成功或失敗的程式碼。 如果狀態值為成功，則傳回值將為非零值。 如果這是失敗狀態碼，傳回值將會是零。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函式 PdhVbIsGoodStatus ( \_ ByVal StatusValue long \_ ) long

## <a name="parameters"></a>參數

<dl> <dt>

*StatusValue* 
</dt> <dd>

要測試的另一個 PDH 函數所傳回的狀態值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果狀態碼為失敗狀態碼，則函數會傳回零。 如果狀態碼為成功狀態碼，則會傳回非零值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




