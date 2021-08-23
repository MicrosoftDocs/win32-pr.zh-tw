---
description: Clone 方法會使用相同的列舉狀態來建立列舉值的複本。 這個方法會實 IEnumMediaTypes：： Clone 方法。
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: 'CEnumMediaTypes 複製方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c624ac933228c769248c2980a250a9f89e9ebdaf386aeff951e70ba966311586
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537301"
---
# <a name="cenummediatypesclone-method"></a>CEnumMediaTypes 複製方法

`Clone`方法會使用相同的列舉狀態來建立列舉值的複本。 這個方法會實 [**IEnumMediaTypes：： Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnum* 
</dt> <dd>

接收新列舉值之 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | 記憶體不足。<br/>                                                     |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標引數。<br/>                                               |
| <dl> <dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt> </dl> | Pin 的狀態已變更，且現在與列舉值不一致。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumMediaTypes 類別**](cenummediatypes.md)
</dt> </dl>

 

 




