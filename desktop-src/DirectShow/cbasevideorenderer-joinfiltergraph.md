---
description: '\_ \_ 從篩選圖形移除篩選時，JoinFilterGraph 方法會傳送 EC 視窗終結事件通知。'
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: 'CBaseVideoRenderer. JoinFilterGraph 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3aed2c887bc7a452cda978e96cd369a71cad4fab60a72e0c914ebe9d9790a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052208"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>CBaseVideoRenderer. JoinFilterGraph 方法

`JoinFilterGraph`從篩選圖形中移除篩選時，方法會傳送 [**EC \_ 視窗 \_**](ec-window-destroyed.md)終結事件通知。

## <a name="syntax"></a>語法


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGraph* 
</dt> <dd>

要加入之篩選圖形的指標。

</dd> <dt>

*pName* \[在\]
</dt> <dd>

要加入之篩選器名稱的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此成員函式會覆寫 [**CBaseFilter：： JoinFilterGraph**](cbasefilter-joinfiltergraph.md) 成員函式。 如果篩選準則離開篩選圖形 (*pGraph* 為 **Null**) ，它會傳送 [**EC \_ 視窗 \_**](ec-window-destroyed.md) 終結事件通知，讓資源管理員不會以焦點物件的形式來保存轉譯器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




