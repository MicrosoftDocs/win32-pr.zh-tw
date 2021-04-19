---
description: SetFilterGraph 方法會指定轉譯引擎要使用的篩選圖形。
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'IRenderEngine：： SetFilterGraph 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981411"
---
# <a name="irenderenginesetfiltergraph-method"></a>IRenderEngine：： SetFilterGraph 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetFilterGraph`方法會指定要用於轉譯引擎的篩選圖形。

## <a name="syntax"></a>語法


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFG* 
</dt> <dd>

篩選圖形的 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | 無效引數。<br/>                   |
| <dl> <dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt> </dl> | 轉譯引擎無法初始化。<br/> |



 

## <a name="remarks"></a>備註

大部分的應用程式都不需要呼叫此方法。 藉由呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法，讓轉譯引擎為您建立圖形更為常見。

如果轉譯引擎已經有篩選圖形，則這個方法會失敗。

絕對不要取出某個轉譯引擎所建立之篩選圖形的指標，然後在另一個轉譯引擎上使用它做為此方法的參數。 這麼做會導致無法預期的結果。

**ConnectFrontEnd** 方法會眼淚任何現有的篩選圖形，但會保留相同的篩選圖形管理員實例。

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

[**IRenderEngine 介面**](irenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




