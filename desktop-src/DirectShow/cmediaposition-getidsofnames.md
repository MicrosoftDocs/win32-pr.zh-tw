---
description: CMediaPosition. GetIDsOfNames 方法-GetIDsOfNames 方法會將一組名稱對應至一組對應的 Dispid。
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: 'CMediaPosition. GetIDsOfNames 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eebd32638afdf957024f54f6a601e95bae274dc4ab9a8265e9a618d635a23530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634791"
---
# <a name="cmediapositiongetidsofnames-method"></a>CMediaPosition. GetIDsOfNames 方法

方法會將 `GetIDsOfNames` 一組名稱對應至一組對應的 dispid。

## <a name="syntax"></a>語法


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* 
</dt> <dd>

保留的。 使用 IID \_ Null。

</dd> <dt>

*rgszNames* 
</dt> <dd>

寬字元字串陣列的位址，其中包含要對應的名稱。

</dd> <dt>

*Cname* 
</dt> <dd>

*RgszNames* 參數所指定的陣列大小。

</dd> <dt>

*lcid* 
</dt> <dd>

要在其中解讀名稱的地區設定內容。 可以是 **Null**。

</dd> <dt>

*rgdispid* 
</dt> <dd>

接收 Dispid 之陣列的指標。 的每個專案都會收到一個識別碼，該識別碼對應至 *rgszNames* 參數中傳遞的其中一個名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                         | 描述                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 成功。<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | 記憶體不足。<br/>                     |
| <dl> <dt>**將 \_ 電子 \_ UNKNOWNNAME**</dt> </dl> | 一或多個名稱未知。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaPosition 類別**](cmediaposition.md)
</dt> </dl>

 

 




