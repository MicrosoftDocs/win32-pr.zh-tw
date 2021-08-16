---
description: 用來通知主機圖形記錄摘要資訊的回呼函數。
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISummaryCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aa4b420f92919fdff2abddf0c172fd25d8a552feb07ba6583fd8621e456808a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844818"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback：： ResultCallback 方法

用來通知主機圖形記錄摘要資訊的回呼函數。

## <a name="syntax"></a>語法


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a>參數

*計數*   
傳回的摘要資訊專案數目。

*count0 \_ summaryItem*   
摘要資訊專案 (的索引鍵/值組) 。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**ISummaryCallback**](/windows/desktop/direct3dtools/isummarycallback)

 

 
