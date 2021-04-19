---
description: 捕獲介面指標並遞增參考計數。 這個方法會實 INonDelegatingUnknown：： NonDelegatingQueryInterface 方法。
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: 'CUnknown. NonDelegatingQueryInterface 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001847"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>CUnknown. NonDelegatingQueryInterface 方法

捕獲介面指標並遞增參考計數。 這個方法會實 **INonDelegatingUnknown：： NonDelegatingQueryInterface** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* 
</dt> <dd>

介面的識別碼。

</dd> <dt>

*Ppv* 
</dt> <dd>

接收介面之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | 物件不支援此介面。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數。<br/>              |



 

## <a name="remarks"></a>備註

**CUnknown** 類別只會公開 **IUknown** 介面。 覆寫此方法以公開其他介面。 如需有關如何覆寫這個方法的詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




