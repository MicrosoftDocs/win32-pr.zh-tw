---
description: Init 方法會初始化物件。
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: 'CSeekingPassThru.Init 方法 (Seekpt .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91d20477f83ec79c6ae6095e81810c98454f9c26521eda995c919867b3e3ac12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953810"
---
# <a name="cseekingpassthruinit-method"></a>CSeekingPassThru.Init 方法

`Init`方法會初始化物件。

## <a name="syntax"></a>語法


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bSupportRendering* \[在\]
</dt> <dd>

指定篩選是否為轉譯器的布林值。 如果篩選器是轉譯器，請使用 **TRUE** 值，否則為 **FALSE** 。

</dd> <dt>

*pPin* 
</dt> <dd>

篩選器輸入釘選上 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | 描述                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 物件已初始化。<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法建立物件。<br/> |



 

## <a name="remarks"></a>備註

如果 *bSupportRendering* 的值為 **TRUE**，這個方法會建立 [**CRendererPosPassThru**](crendererpospassthru.md) 類別的實例。 否則，它會建立 [**CPosPassThru**](cpospassthru.md) 類別的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Seekpt (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSeekingPassThru 類別**](cseekingpassthru.md)
</dt> </dl>

 

 




