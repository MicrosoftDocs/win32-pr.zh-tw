---
description: SrcAdd 方法會將來源新增至追蹤。
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'IAMTimelineTrack：： SrcAdd 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e705f840a073ee6796776f6f68c7b57df0bd972facf8f7a586792519735bfb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998748"
---
# <a name="iamtimelinetracksrcadd-method"></a>IAMTimelineTrack：： SrcAdd 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SrcAdd`方法會將來源新增至追蹤。

## <a name="syntax"></a>語法


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Psrc* 
</dt> <dd>

來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 \_如果物件不是來源物件，則傳回 E NOINTERFACE。 否則，會傳回 **HRESULT** 值，指出錯誤的原因。

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先設定來源的開始和停止時間。  (呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md)。 ) 

目前，DES 無法同時轉譯超過75個以視訊壓縮管理員壓縮的來源 (BC-VCM-LVM-HYPERV) 編解碼器。 此外，如果整個專案包含75以上的來源，您必須使用動態重新連接，否則 DES 無法預覽專案。 如需詳細資訊，請參閱 [**IRenderEngine：： SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineTrack 介面**](iamtimelinetrack.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




