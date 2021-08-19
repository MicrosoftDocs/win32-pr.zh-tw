---
description: RenderOutputPins 方法會建立篩選圖形的預覽部分。
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'IRenderEngine：： RenderOutputPins 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b81ea650d805c8ed2e42797f4dffdd9851eb3f072cff0abb05f54c4581684bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818560"
---
# <a name="irenderenginerenderoutputpins-method"></a>IRenderEngine：： RenderOutputPins 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`RenderOutputPins`方法會建立篩選圖形的預覽部分。

## <a name="syntax"></a>語法


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 以下是可能的值：



| 傳回碼                                                                                                  | 描述                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                                                        |
| <dl> <dt>**未轉譯 VFW \_ S \_ 音訊 \_ \_**</dt> </dl>  | 無法播放音訊串流。<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | 無效引數。<br/>                                               |
| <dl> <dt>**E \_ 轉譯 \_ 引擎 \_ 已 \_ 中斷**</dt> </dl> | 因為未成功轉譯專案，所以操作失敗。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>                 | 非預期的錯誤。<br/>                                               |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來建立圖形的前端。 若要執行預覽以外的作業，請不要呼叫這個方法。 請改為呼叫 [**IRenderEngine：： GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) 來取得輸出圖釘的指標。

如果使用者的電腦上沒有音效卡，這個方法會傳回未轉譯的 VFW \_ s \_ 音訊 \_ \_ 。 在此情況下，將不會有音訊預覽，但影片預覽不會受到影響。

如果釘選來自影片群組，這個方法會建立影片視窗。 呼叫執行緒必須分派訊息（例如，移動視窗），或在視窗的工作區中回應滑鼠點擊。

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

[**IRenderEngine 介面**](irenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




