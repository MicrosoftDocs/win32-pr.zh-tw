---
description: GetSampleGrabber 方法會抓取 ISampleGrabber 介面的指標，讓應用程式能夠從媒體資料流程中取出個別樣本。
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'IMediaDet：： GetSampleGrabber 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994686"
---
# <a name="imediadetgetsamplegrabber-method"></a>IMediaDet：： GetSampleGrabber 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetSampleGrabber` [**ISampleGrabber**](isamplegrabber.md) 介面的指標，此介面可讓應用程式從媒體資料流程中取出個別樣本。

## <a name="syntax"></a>語法


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppVal* \[擴展\]
</dt> <dd>

接收 [**ISampleGrabber**](isamplegrabber.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

呼叫 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) ，然後再呼叫這個方法。 [**ISampleGrabber**](isamplegrabber.md)介面可讓您從資料流程中取出個別的媒體範例。 如果您只需要影片框架中的點陣圖，請改為呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md) 方法。 **ISampleGrabber** 介面更有彈性，但應用程式需要更多工作。

如果這個方法成功，則傳回的 [**ISampleGrabber**](isamplegrabber.md) 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

[**IMediaDet 介面**](imediadet.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




