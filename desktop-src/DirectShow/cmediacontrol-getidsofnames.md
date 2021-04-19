---
description: 將單一成員函式和一組選擇性的參數對應至一組對應的整數分派識別碼 (Dispid) ，可在後續呼叫 CMediaControl：： Invoke 成員函式時使用。
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: 'CMediaControl. GetIDsOfNames 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f906db9540f0429e1e7831284e55edf8c29b6a03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000813"
---
# <a name="cmediacontrolgetidsofnames-method"></a>CMediaControl. GetIDsOfNames 方法

將單一成員函式和一組選擇性的參數對應至一組對應的整數分派識別碼 (Dispid) ，可在後續呼叫 [**CMediaControl：： Invoke**](cmediacontrol-invoke.md) 成員函式時使用。

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

參考識別碼。 保留供未來使用。 必須是 **Null**。

</dd> <dt>

*rgszNames* 
</dt> <dd>

要對應之名稱陣列的指標位址。

</dd> <dt>

*Cname* 
</dt> <dd>

要對應的名稱計數。

</dd> <dt>

*lcid* 
</dt> <dd>

要在其中解讀名稱的地區設定內容。

</dd> <dt>

*rgdispid* 
</dt> <dd>

呼叫端配置陣列的指標，其中的每個專案都包含對應至 *rgszNames* 陣列中傳遞之其中一個名稱的識別碼。 第一個元素代表成員名稱;後續的元素代表每個成員的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                                            | Description                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**以 \_ 電子 \_ 不明 \_ CLSID**</dt> </dl> | 無法辨識 CLSID。<br/>                                                                                                             |
| <dl> <dt>**將 \_ 電子 \_ UNKNOWNNAME**</dt> </dl>    | 一或多個名稱未知。 傳回的 Dispid 包含 \_ 每個對應至未知名稱之專案的 dispid 未知。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | 記憶體不足。<br/>                                                                                                                            |
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>                                                                                                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaControl 類別**](cmediacontrol.md)
</dt> </dl>

 

 




