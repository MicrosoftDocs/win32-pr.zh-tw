---
description: PdhVbCreateCounterPathList 函式會顯示 [效能計數器流覽] 對話方塊，讓使用者選取數個效能計數器。 接著，每個選取的計數器路徑都必須使用 PdhVbGetCounterPathFromList 函式來讀取。
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849290"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>PdhVbCreateCounterPathList 函式

**PdhVbCreateCounterPathList** 函式會顯示 [效能計數器流覽] 對話方塊，讓使用者選取數個效能計數器。 接著，每個選取的計數器路徑都必須使用 [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) 函式來讀取。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函式 PdhVbCreateCounterPathList ( \_ Byval DetailLevel，只要是 \_ 字串 \_ ) 

## <a name="parameters"></a>參數

<dl> <dt>

*DetailLevel* 
</dt> <dd>

要在對話方塊中顯示的計數器類型。 使用下列其中一個值。



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

函數會傳回使用者選取的計數器路徑數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




