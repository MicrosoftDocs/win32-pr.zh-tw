---
description: 回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 69f577ec182144a59a7c879a56e8222911ec3fa56b979b5d7a6e7d1e68982ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484951"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback：： ResultCallback 方法

回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。

## <a name="syntax"></a>語法


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>參數

*frameNumber*   
畫面格編號。

*寬度*   
框架的寬度。

*高度*   
框架的高度。

*renderTargetPtr*   
結果來源的呈現目標。 它一律是框架緩衝區要求所指定的位置，或者，如果不是繪製呼叫，則第一個 RTV 會 bount 至輸出來源。

*frameDuraction*   
未使用。

*大小*   
輸出緩衝區的大小（以位元組為單位）。

*count5 \_ 緩衝區*   
以 R8G8B8A8 UNORM 格式呈現的轉譯目標內容 \_ 。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
