---
description: 回呼函數，用來通知主機事件清單中事件的相關資訊。
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1b6cf33869fce9dc51df8dcd58f98b0cc17a5f44
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623964"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback：： ResultCallback 方法

回呼函數，用來通知主機事件清單中事件的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a>參數

*frameNumber*   
與事件相關聯的框架編號。

*numElements*   
所有事件的所有資料行中的總欄位數。

*numRows*   
結果中的事件數目。

*numColumns*   
每個資料列中 (欄位) 的資料行數目。

*count1 \_ pRowData*   
事件的相關資訊;每個事件的每個欄位都有一個專案。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IFrameEventsCallback**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
