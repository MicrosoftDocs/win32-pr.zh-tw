---
description: GetStdDev 方法會根據每個畫面格的統計資料，來估計每個框架的到期時間和實際轉譯的標準差（以毫秒為單位）。
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: 'CBaseVideoRenderer. GetStdDev 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f7b6ab85000f537179fcc9ae6b979194ae4e975ea2b394d0c58afb8515158aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157080"
---
# <a name="cbasevideorenderergetstddev-method"></a>CBaseVideoRenderer. GetStdDev 方法

方法會根據每個畫面格的 `GetStdDev` 統計資料，來估計每個框架的到期時間和實際轉譯的標準差（以毫秒為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nSamples* 
</dt> <dd>

整數值，其中包含影片轉譯器收到的影片樣本數。

</dd> <dt>

*piResult* 
</dt> <dd>

整數值的指標，該整數值會包含標準差。

</dd> <dt>

*llSumSq* 
</dt> <dd>

值，表示所有轉譯的影片樣本的標準差（以毫秒為單位）。 值越低，呈現的一致性就越一致。

</dd> <dt>

*iTot* 
</dt> <dd>

值，表示所有轉譯的影片樣本的戳記時間和轉譯時間之間的平均值（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




