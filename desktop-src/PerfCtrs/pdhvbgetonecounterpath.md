---
description: PdhVbGetOneCounterPath 函式會顯示一個對話方塊，讓使用者流覽可用的效能計數器，並選取一個計數器。
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: da6cc5b476373a55135d91d21163f15cb04379fff9d7c7c2cf1342451a5a201d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061156"
---
# <a name="pdhvbgetonecounterpath-function"></a>PdhVbGetOneCounterPath 函式

**PdhVbGetOneCounterPath** 函式會顯示一個對話方塊，讓使用者流覽可用的效能計數器，並選取一個計數器。 選取的計數器會在 *PathString* 變數中傳回。 在呼叫此函式之前，必須先將 *PathString* 變數進行維度和初始化，而且維度大小必須由 *PathLength* 變數表示。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函數 PdhVbGetOneCounterPath ( \_ Byval PathString As string， \_ Byval PathLength long，byval DetailLevel long，Byval \_ \_ CaptionString as string \_ ) long

## <a name="parameters"></a>參數

<dl> <dt>

*PathString* 
</dt> <dd>

初始化的字串變數，用來接收使用者選取的計數器路徑。

</dd> <dt>

*PathLength* 
</dt> <dd>

初始化的 PathString 長度。

</dd> <dt>

*DetailLevel* 
</dt> <dd>

要在對話方塊中顯示的計數器類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                               | 意義                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**效能 \_ 詳細資料 \_ ADVANCED**</dt> </dl> | Advanced user 可能瞭解的計數器，以及新手使用者的計數器。<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**效能 \_ 詳細資料 \_ 專家**</dt> </dl>       | 專家使用者和軟體發展人員可能會瞭解的計數器，以及新手和 advanced 使用者的計數器。<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**效能 \_ 詳細資料 \_ 新手**</dt> </dl>       | 只有新手使用者可能會瞭解的計數器。<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**效能 \_ 詳細資料 \_ 嚮導**</dt> </dl>       | 系統中的所有計數器。<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

包含要在對話方塊標題列中顯示之文字的字串變數。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回寫入 *PathString* 緩衝區的字元數。

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

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




