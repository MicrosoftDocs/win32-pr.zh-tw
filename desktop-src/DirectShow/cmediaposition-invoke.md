---
description: Invoke 方法可讓您存取物件所公開的屬性和方法。
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: 'CMediaPosition： Invoke 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001177"
---
# <a name="cmediapositioninvoke-method"></a>CMediaPosition 方法

`Invoke`方法可讓您存取物件所公開的屬性和方法。

## <a name="syntax"></a>語法


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dispidMember* 
</dt> <dd>

成員的識別碼。 使用 [**CMediaPosition：： GetIDsOfNames**](cmediaposition-getidsofnames.md) 取得分派識別碼。

</dd> <dt>

*riid* 
</dt> <dd>

保留供未來使用。 必須是 IID \_ Null。

</dd> <dt>

*lcid* 
</dt> <dd>

要在其中解讀引數的地區設定內容。

</dd> <dt>

*wFlags* 
</dt> <dd>

描述呼叫之內容的旗標。

</dd> <dt>

*pdispparams* 
</dt> <dd>

**DIPPARAMS** 結構的指標，其中包含引數。

</dd> <dt>

*pvarResult* 
</dt> <dd>

接收結果之 **變異** 的指標，如果呼叫端不需要任何結果，則為 **Null** 。

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

接收例外狀況資訊之結構的指標。

</dd> <dt>

*>puargerr* 
</dt> <dd>

變數的指標，此變數會接收導致錯誤之第一個引數的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                              | Description                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 成功。<br/>                              |
| <dl> <dt>**將 \_ 電子 \_ UNKNOWNINTERFACE**</dt> </dl> | *Riid* 參數不是 IID \_ Null<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaPosition 類別**](cmediaposition.md)
</dt> </dl>

 

 




