---
description: 抓取類型資訊物件，此物件可以取得介面的類型資訊。
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: 'CMediaControl. GetTypeInfo 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe393922206744c23b534bf8d701d6292736c65a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998401"
---
# <a name="cmediacontrolgettypeinfo-method"></a>CMediaControl. GetTypeInfo 方法

抓取類型資訊物件，此物件可以取得介面的類型資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*itinfo* 
</dt> <dd>

要傳回的類型資訊。 傳遞零以取得 **IDispatch** 實作為的型別資訊。

</dd> <dt>

*lcid* 
</dt> <dd>

類型資訊的地區設定識別碼。 針對支援當地語系化成員名稱的類別，物件可能會針對不同的語言傳回不同的類型資訊。 對於不支援當地語系化成員名稱的類別，可以忽略這個參數。

</dd> <dt>

*>pptinfo* 
</dt> <dd>

所要求之類型資訊物件的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果 *>pptinfo* 無效，則傳回 E 指標。 \_ \_ 如果 *itinfo* 不是零，則傳回型別 E ELEMENTNOTFOUND。 \_如果成功，則傳回 S OK。 否則，會傳回其中一個呼叫的 **HRESULT** ，以抓取型別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaControl 類別**](cmediacontrol.md)
</dt> </dl>

 

 




