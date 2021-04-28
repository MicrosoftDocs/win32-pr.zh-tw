---
description: CMediaPosition. GetTypeInfo 方法-GetTypeInfo 方法會抓取物件的型別資訊，然後用它來取得介面的型別資訊。
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: 'CMediaPosition. GetTypeInfo 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099136"
---
# <a name="cmediapositiongettypeinfo-method"></a>CMediaPosition. GetTypeInfo 方法

`GetTypeInfo`方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。

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

要傳回的類型資訊。 必須為零。

</dd> <dt>

*lcid* 
</dt> <dd>

地區設定識別項。

</dd> <dt>

*>pptinfo* 
</dt> <dd>

接收 **ITypeInfo** 指標之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                             | Description                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                            |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標引數。<br/>          |
| <dl> <dt>**輸入 \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | *Itinfo* 參數不是零。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaPosition 類別**](cmediaposition.md)
</dt> </dl>

 

 




