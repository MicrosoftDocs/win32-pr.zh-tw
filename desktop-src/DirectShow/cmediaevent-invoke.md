---
description: CMediaEvent 方法-提供對物件所公開之屬性和方法的存取。
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: 'CMediaEvent： Invoke 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37fadefe3163ed4211b8112ec17cc1cfb3fb3625b4aba207db06a25de3e27b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655222"
---
# <a name="cmediaeventinvoke-method"></a>CMediaEvent 方法

提供物件所公開的屬性和方法的存取權。

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

成員的識別碼。 使用 [**CMediaEvent：： GetIDsOfNames**](cmediaevent-getidsofnames.md) 或物件的檔以取得分派識別碼。

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

描述呼叫內容的旗標 `CMediaEvent::Invoke` 。

</dd> <dt>

*pdispparams* 
</dt> <dd>

結構的指標，此結構包含引數陣列、具名引數的引數分派識別碼陣列，以及陣列中專案數目的計數。

</dd> <dt>

*pvarResult* 
</dt> <dd>

要儲存結果之位置的指標，如果呼叫端預期沒有任何結果，則為 **Null** 。

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

包含例外狀況資訊之結構的指標。

</dd> <dt>

*>puargerr* 
</dt> <dd>

在 **DISPPARAMS** 結構的 **>rgvarg** 陣列中，第一個引數索引的指標，其發生錯誤。 如需 **DISPPARAMS** 的詳細資訊，請參閱 Platform SDK。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_ \_ 如果 *RIID* 不是 IID Null，則會傳回 \_ 空的 E UNKNOWNINTERFACE。 如果呼叫失敗，則從 [**CMediaEvent：： GetTypeInfo**](cmediaevent-gettypeinfo.md) 傳回其中一個錯誤碼。 否則，會從呼叫 **IDispatch：： Invoke** 傳回 **HRESULT** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaEvent 類別**](cmediaevent.md)
</dt> </dl>

 

 




