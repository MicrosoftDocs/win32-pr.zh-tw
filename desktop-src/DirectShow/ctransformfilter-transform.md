---
description: 轉換方法會轉換輸入範例，以產生輸出範例。
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: 'CTransformFilter 轉換方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990166"
---
# <a name="ctransformfiltertransform-method"></a>CTransformFilter 轉換方法

`Transform`方法會轉換輸入範例，以產生輸出範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*針* 
</dt> <dd>

輸入範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> <dt>

*彆扭* 
</dt> <dd>

輸出範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

基類傳回 E 非 \_ 預期的。

衍生類別應該會傳回 **HRESULT** 值，表示成功或失敗。 可能的值包括下表所示的值。



| 傳回碼                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 請勿傳遞此範例。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                    |



 

## <a name="remarks"></a>備註

覆寫此方法以產生輸出資料。 從 *pIn* 參數所指定的範例讀取輸入資料，並將新的資料寫入 *不悅* 參數所指定的範例中。

在篩選準則呼叫這個方法之前，它會將屬性從輸入範例複製到輸出範例。 `Transform`方法應該使用 **IMediaSample** 方法或 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)介面 (（如果有) 的話），來設定兩個範例之間有差異的任何屬性。

如果篩選器不應該傳遞此範例 (例如，為了支援品質控制) ，此方法應該會傳回 \_ FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




