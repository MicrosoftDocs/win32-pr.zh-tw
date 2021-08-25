---
description: PdhVbGetCounterPathFromList 函式會將索引參數所參考的計數器路徑從使用者建立的計數器路徑清單複製到 PdhVbCreateCounterPathList 函數的最新呼叫。
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 85760bbcdcc81204340004304be1f0c14bf9bcbbbd7a5b59eebf47a25f7b15c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033778"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>PdhVbGetCounterPathFromList 函式

**PdhVbGetCounterPathFromList** 函式會將 *索引* 參數所參考的計數器路徑從使用者建立的計數器路徑清單複製到 [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)函數的最新呼叫。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函式 PdhVbGetCounterPathFromList ( 的 \_ Byval 索引為 long，以字串形式的 \_ byval 緩衝區， \_ \_ ) 長時間的 byval BufferLength

## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

要取出的計數器路徑索引。 這必須是大於或等於1，且小於或等於 [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) 函數所傳回值的值。

</dd> <dt>

*Buffer* 
</dt> <dd>

經過維度和初始化的字串，將會接收對應至 Index 參數值的計數器路徑。

</dd> <dt>

*BufferLength* 
</dt> <dd>

緩衝區所參考的字串中所能容納的最大字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回復制到緩衝區的字元數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




