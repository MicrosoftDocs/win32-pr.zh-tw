---
description: GetVideoPaletteEntries 方法會抓取影片的某個範圍元件專案。
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: 'CBaseControlVideo. GetVideoPaletteEntries 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991341"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>CBaseControlVideo. GetVideoPaletteEntries 方法

方法會抓取 `GetVideoPaletteEntries` 影片的某個範圍的元件專案。

## <a name="syntax"></a>語法


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartIndex* 
</dt> <dd>

以零為基底的啟動元件專案。

</dd> <dt>

*項目* 
</dt> <dd>

需要的專案數目。

</dd> <dt>

*pRetrieved* 
</dt> <dd>

所取得色彩數目的指標。

</dd> <dt>

*pPalette* 
</dt> <dd>

色彩的輸出緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR; 如果 \_ 影片樣本沒有色彩調色板，則會傳回 VFW e \_ NO \_ 調色板; 如果沒有足夠的 \_ \_ 記憶體可用，則為 e OUTOFMEMORY; 如果沒有可用的記憶體， \_ 則為 e INVALIDARG; 如果選擇區中沒有色彩，則 \_ 為 FALSE。

## <a name="remarks"></a>備註

此成員函式會以使用者配置的陣列形式傳回影片的目前調色板。 若要保持一致，請使用 Win32 **PALETTEENTRY** 結構中的成員來傳回色彩，而不是 **RGBQUAD** (結構中的成員，但參數是 **長**) 。 記憶體是由呼叫端配置，因此只要再複製一次即可。 判斷要求的專案數和開始位置位移都有效。 如果專案數評估為零，則會傳回 \_ FALSE 代碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




