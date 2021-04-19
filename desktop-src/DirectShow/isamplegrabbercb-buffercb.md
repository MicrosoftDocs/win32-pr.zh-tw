---
description: BufferCB 方法是可接收範例緩衝區指標的回呼方法。
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'ISampleGrabberCB：： BufferCB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001936"
---
# <a name="isamplegrabbercbbuffercb-method"></a>ISampleGrabberCB：： BufferCB 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**BufferCB** 方法是可接收範例緩衝區指標的回呼方法。

## <a name="syntax"></a>語法


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SampleTime* 
</dt> <dd>

取樣的開始時間（以秒為單位）。

</dd> <dt>

*pBuffer* 
</dt> <dd>

包含範例資料之緩衝區的指標。 資料的格式取決於範例抓取器輸入釘選的媒體類型。 若要取得媒體類型，請呼叫 [**ISampleGrabber：： GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md)。

</dd> <dt>

*BufferLen* 
</dt> <dd>

*PBuffer* 所指向之緩衝區的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，否則傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此回呼方法會接收最新媒體範例中的資料指標。

> [!Note]  
> 這個方法會接收原始範例資料的指標，而不是複本。 原始檔案不正確地指定 *pBuffer* 包含一份資料複本。

 

若要設定回呼，請呼叫 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**ISampleGrabberCB 介面**](isamplegrabbercb.md)
</dt> </dl>

 

 




