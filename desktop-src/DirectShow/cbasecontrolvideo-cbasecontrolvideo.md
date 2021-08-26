---
description: CBaseControlVideo。 CBaseControlVideo 函式-函數方法。
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: 'CBaseControlVideo. CBaseControlVideo (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbd9ed452dbf0c0091c3f1813f6f671c476dfa52e31b402440a3b1d19db2d3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057368"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>CBaseControlVideo. CBaseControlVideo 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFilter* 
</dt> <dd>

擁有媒體篩選物件的指標。

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

要用於鎖定的重要區段指標。

</dd> <dt>

*pName* 
</dt> <dd>

物件描述的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

如果物件是匯總的一部分，則為控制 **IUnknown** 介面的指標;否則，必須是 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 HRESULT 值，指出函式方法的成功或失敗。

</dd> </dl>

## <a name="remarks"></a>備註

物件會實 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 控制項介面。

[**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)中這個類別所執行的所有介面方法都需要正確連接篩選。 基於這個理由，類別會傳遞給與其進行同步處理的 pin。 每當呼叫介面方法時，物件就會判斷該釘選仍連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




