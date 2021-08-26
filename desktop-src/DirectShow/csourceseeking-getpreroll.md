---
description: GetPreroll 方法會捕獲預先進行的時間。 這個方法會實 IMediaSeeking：： GetPreroll 方法。
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: 'CSourceSeeking. GetPreroll 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2d20c4487f0969a5abaf689f7c5c712e6fbb7fd83ceb7484694a3eec8599698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083958"
---
# <a name="csourceseekinggetpreroll-method"></a>CSourceSeeking. GetPreroll 方法

方法會取出預先進行 `GetPreroll` 的時間。 這個方法會實 [**IMediaSeeking：： GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPreroll* 
</dt> <dd>

接收預先提供時間之變數的指標。 值設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | 描述                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




