---
description: PdhVbOpenQuery 函式會建立並初始化用來管理效能資料集合的唯一查詢結構。
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 70d207696f68b9ef86ba0bae1f596826bd6e400d05d011b330f67241e186f5eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962388"
---
# <a name="pdhvbopenquery-function"></a>PdhVbOpenQuery 函式

**PdhVbOpenQuery** 函式會建立並初始化用來管理效能資料集合的唯一查詢結構。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函式 PdhVbOpenQuery ( \_ ByVal QueryHandle long \_ ) long

## <a name="parameters"></a>參數

<dl> <dt>

*QueryHandle* 
</dt> <dd>

在呼叫函式之前，已清除 (等於 0) 的變數，如果函式成功，則會包含所建立並開啟之查詢的唯一識別碼。 這個控制碼是在後續呼叫其他 PDH 函數來識別查詢時使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回等於 ERROR SUCCESS 的 **長** 整數 \_ ，以及 *QueryHandle* 變數中的新控制碼。

如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。 以下是可能的值。



| 傳回碼                                                                                                     | 描述                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**PDH \_ 不正確 \_ 引數**</dt> </dl>           | 引數無效或不正確。<br/>             |
| <dl> <dt>**PDH \_ 記憶體 \_ 配置 \_ 失敗**</dt> </dl> | 無法配置暫存記憶體緩衝區。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

