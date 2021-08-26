---
description: FindPin 方法會使用指定的識別碼抓取 pin。
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: 'CBaseRenderer. FindPin 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f639e5d68b11b6a7a65ccfe0d0c6465f822d591b0c4dfd0f4916072fde40856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043768"
---
# <a name="cbaserendererfindpin-method"></a>CBaseRenderer. FindPin 方法

`FindPin`方法會使用指定的識別碼抓取 pin。

## <a name="syntax"></a>語法


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

常數、以 null 結尾的寬字元字串的指標，可識別 pin。 必須是 L "In"。

</dd> <dt>

*ppPin* 
</dt> <dd>

接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標的變數位址。 如果方法失敗， *\* ppPin* 會設為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                       | 描述                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>         | **Null** 指標引數。<br/> |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 找不到。<br/>                 |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseFilter：： FindPin**](cbasefilter-findpin.md) 方法。 篩選器的唯一 pin (輸入 pin) 名稱為 "In"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




