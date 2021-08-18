---
description: BreakConnect 方法會從連接釋放輸入的 pin。
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: 'CBaseRenderer. BreakConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cefaa91578f397a5ce967dc9cb6200acbe45f016e81f4552b9d185ad9ffa2609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044058"
---
# <a name="cbaserendererbreakconnect-method"></a>CBaseRenderer. BreakConnect 方法

`BreakConnect`方法會從連接釋放輸入的 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                         | 描述                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Pin 未連接。<br/>  |
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 成功。<br/>                    |
| <dl> <dt>**VFW \_ E \_ 未 \_ 停止**</dt> </dl> | 篩選仍處於使用中。<br/> |



 

## <a name="remarks"></a>備註

篩選器的輸入圖釘會從它自己的方法內呼叫這個方法 `BreakConnect` 。  (如需詳細資訊，請參閱 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md)。 ) 篩選準則會執行一些內部的簿記，例如重設資料流程結尾旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




