---
description: PdhVbAddCounter 函式會在指定的查詢物件中建立計數器專案，並在成功完成時傳回該計數器的控制碼。
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6605e2fb02edad23831b22334b960eaa2e89f23206673608500f248452094ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061146"
---
# <a name="pdhvbaddcounter-function"></a>PdhVbAddCounter 函式

**PdhVbAddCounter** 函式會在指定的查詢物件中建立計數器專案，並在成功完成時傳回該計數器的控制碼。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函數 PdhVbAddCounter ( \_ Byval QueryHandle long，Byval \_ CounterPath as String，long \_ \_ ) long

## <a name="parameters"></a>參數

<dl> <dt>

*QueryHandle* 
</dt> <dd>

要指派此計數器的查詢識別碼。 [**PdhVbOpenQuery**](pdhvbopenquery.md)函數會傳回這個值。

</dd> <dt>

*CounterPath* 
</dt> <dd>

文字字串，指定要加入至查詢的計數器路徑名稱。 此字串的內容必須是有效的計數器路徑，如同從計數器瀏覽器或其他來源取得。

</dd> <dt>

*CounterHandle* 
</dt> <dd>

在查詢中識別此計數器的唯一參考。 在呼叫函式之前，此變數必須初始化為零。 只有當函式成功完成時，才會在傳回時包含有效的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回等於 ERROR SUCCESS 的 **長** 整數 \_ ，以及 *CounterHandle* 變數中的新控制碼。

如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。 以下是可能的值。



| 傳回碼                                                                                                     | 描述                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ 不正確 \_ 引數**</dt> </dl>           | 一或多個引數無效或不正確。<br/>              |
| <dl> <dt>**PDH \_ 記憶體 \_ 配置 \_ 失敗**</dt> </dl> | 無法配置記憶體緩衝區。<br/>                            |
| <dl> <dt>**PDH \_ 不正確 \_ 控制碼**</dt> </dl>             | 查詢控制碼無效。<br/>                                     |
| <dl> <dt>**PDH \_ CSTATUS \_ 沒有 \_ 計數器**</dt> </dl>        | 找不到指定的計數器。<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ 沒有 \_ 物件**</dt> </dl>         | 找不到指定的物件。<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ 沒有 \_ 電腦**</dt> </dl>        | 無法建立電腦專案。<br/>                             |
| <dl> <dt>**PDH \_ CSTATUS \_ 不良 \_ COUNTERNAME**</dt> </dl>   | 傳入了空的計數器名稱路徑字串。<br/>                   |
| <dl> <dt>**\_ \_ 找不到 PDH 函數 \_**</dt> </dl>        | 無法判斷此計數器的計算函數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

