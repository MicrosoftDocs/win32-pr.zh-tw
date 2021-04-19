---
description: SetBufferSamples 方法會指定是否要在經過篩選時，將範例資料複製到緩衝區。
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'ISampleGrabber：： SetBufferSamples 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990710"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>ISampleGrabber：： SetBufferSamples 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**SetBufferSamples** 方法會指定是否要在經過篩選時，將範例資料複製到緩衝區。

## <a name="syntax"></a>語法


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BufferThem* 
</dt> <dd>

指定是否要緩衝範例資料的布林值。 若 **為 TRUE**，則篩選會將範例資料複製到內部緩衝區中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

若要取得複製的緩衝區，請呼叫 [**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)。

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

[使用範例捕獲](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber 介面**](isamplegrabber.md)
</dt> </dl>

 

 




