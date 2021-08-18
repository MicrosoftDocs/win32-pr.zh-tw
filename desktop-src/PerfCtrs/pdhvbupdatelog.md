---
description: PdhVbUpdateLog 函數函數會更新目前的查詢，並將新的資料寫入記錄檔。 此函數會呼叫 PdhUpdateLog。
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c7bf8af71d3a0f5cd20a84ef0f1532806e3d3e8d268bd2d322d617534b533cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033608"
---
# <a name="pdhvbupdatelog-function"></a>PdhVbUpdateLog 函式

**PdhVbUpdateLog** 函數函數會更新目前的查詢，並將新的資料寫入記錄檔。 此函數會呼叫 [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

Function PdhVbUpdateLog ( \_ Byval HLog 作為 PDH \_ hLog， \_ BYVAL szUserString as LPCTSTR \_ ) 

## <a name="parameters"></a>參數

<dl> <dt>

*hLog* \[在\]
</dt> <dd>

要更新之記錄檔的控制碼。 [**PdhVbOpenLog**](pdhvbopenlog.md)函數會傳回這個控制碼。

</dd> <dt>

*szUserString* \[在\]
</dt> <dd>

字串的指標，指定要加入至記錄檔的資料。 這通常用於記錄檔中的批註。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函數成功，它會傳回0。

如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。 以下是可能的值。



| 傳回碼                                                                                                | 描述                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ \_ 緩衝區不足**</dt> </dl>   | 要求的資料大於提供的緩衝區。 無法傳回要求的資料。<br/> |
| <dl> <dt>**PDH \_ 不正確 \_ 引數**</dt> </dl>      | 一或多個字串緩衝區的大小不正確。<br/>                                  |
| <dl> <dt>**PDH \_ 不正確 \_ 控制碼**</dt> </dl>        | 控制碼不是有效的 PDH 物件。<br/>                                                       |
| <dl> <dt>**PDH \_ 記錄 \_ 檔 \_ 開啟 \_ 錯誤**</dt> </dl> | 無法開啟指定的記錄檔。<br/>                                                      |
| <dl> <dt>**\_ \_ \_ 找不到 PDH 檔案**</dt> </dl>       | 找不到指定的檔案。<br/>                                                          |



 

## <a name="remarks"></a>備註

必須有目前開啟的查詢，而且必須在呼叫此函式之前，將所需的計數器加入至該查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

