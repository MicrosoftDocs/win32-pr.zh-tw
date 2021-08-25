---
description: GetMediaPositionInterface 方法會抓取篩選器的 IMediaPosition 和 IMediaSeeking 介面指標。
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: 'CBaseRenderer. GetMediaPositionInterface 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12e15b297f78b3386ae9ad31e749858bad14b87e59e938ac02a3cf3a9ca002a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872328"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>CBaseRenderer. GetMediaPositionInterface 方法

方法會抓取 `GetMediaPositionInterface` 篩選器的 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面指標。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* 
</dt> <dd>

介面的參考識別碼。

</dd> <dt>

*Ppv* 
</dt> <dd>

接收介面指標之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                   | 描述                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>     |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | 不支援的介面。<br/> |



 

## <a name="remarks"></a>備註

篩選準則會將所有搜尋命令委派給 [**CRendererPosPassThru**](crendererpospassthru.md) 物件，並將它們傳遞至上游。 這個方法會建立 **CRendererPosPassThru** 物件（如果尚不存在），並針對要求的介面進行查詢。

[**CBaseRenderer：： m \_ pPosition**](cbaserenderer-m-pposition.md)成員變數會將指標儲存至 **CRendererPosPassThru** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




