---
description: PdhVbGetCounterPathElements 函式會將完整的效能計數器路徑字串剖析成其個別元素。
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: fecd9ecac573ecc1a5afabcfc4a14bf6fd1ca5cee7b44387ea910b0cf1a5820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011326"
---
# <a name="pdhvbgetcounterpathelements-function"></a>PdhVbGetCounterPathElements 函式

**PdhVbGetCounterPathElements** 函式會將完整的效能計數器路徑字串剖析成其個別元素。 在此函式中使用字串變數時，每個字串變數的大小必須相同 (*BufferSize*) 和已進行維度和初始化。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函數 PdhVbGetCounterPathElements ( \_ Byval PathString As string， \_ Byval MachineName as string，byval ObjectName as string，byval InstanceName as string，Byval ParentInstance as string，Byval \_ \_ \_ \_ CounterName as \_ \_ string，byval 的 long ) 

## <a name="parameters"></a>參數

<dl> <dt>

*PathString* 
</dt> <dd>

要分解成其個別元素的計數器路徑字串。

</dd> <dt>

*MachineName* 
</dt> <dd>

要接收電腦名稱稱的字串。

</dd> <dt>

*ObjectName* 
</dt> <dd>

要接收物件名稱的字串。

</dd> <dt>

*InstanceName* 
</dt> <dd>

要接收實例名稱的字串（如果使用的話）。

</dd> <dt>

*ParentInstance* 
</dt> <dd>

要接收父實例的字串（如果使用的話）。

</dd> <dt>

*CounterName* 
</dt> <dd>

要接收計數器名稱的字串。

</dd> <dt>

*BufferSize* 
</dt> <dd>

當做此函式呼叫之參數使用的每個字串變數大小上限。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回相當於 ERROR SUCCESS 的 **長** 整數 \_ 。

如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。 以下是可能的值。



| 傳回碼                                                                                                     | 描述                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ 不正確 \_ 引數**</dt> </dl>           | 一或多個字串緩衝區的大小不正確。<br/>                          |
| <dl> <dt>**PDH \_ 更多 \_ 資料**</dt> </dl>                  | 一或多個計數器路徑元素對傳回緩衝區長度而言太大。<br/> |
| <dl> <dt>**PDH \_ 記憶體 \_ 配置 \_ 失敗**</dt> </dl> | 無法配置暫存記憶體緩衝區。<br/>                                   |



 

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

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

