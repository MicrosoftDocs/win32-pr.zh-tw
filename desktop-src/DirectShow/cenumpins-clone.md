---
description: Clone 方法會使用相同的列舉狀態來建立列舉值的複本。 這個方法會實 IEnumPins：： Clone 方法。
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: 'CEnumPins 複製方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a0d14f0caf30f6037d53639ff54d2e21d6d0fb0eee5cfa493aba248e84d48e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688608"
---
# <a name="cenumpinsclone-method"></a>CEnumPins 複製方法

`Clone`方法會使用相同的列舉狀態來建立列舉值的複本。 這個方法會實 [**IEnumPins：： Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnum* 
</dt> <dd>

接收新列舉值之 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | 記憶體不足。<br/>                                                        |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標引數。<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt> </dl> | 篩選的狀態已變更，且現在與列舉值不一致。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumPins 類別**](cenumpins.md)
</dt> </dl>

 

 




