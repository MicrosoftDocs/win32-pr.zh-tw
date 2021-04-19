---
description: ValidateBitmapInfoHeader 函式會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤，檢查 BITMAPINFOHEADER 結構。
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: 'ValidateBitmapInfoHeader 函式 (Checkbmi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999398"
---
# <a name="validatebitmapinfoheader-function"></a>ValidateBitmapInfoHeader 函式

`ValidateBitmapInfoHeader`函數會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤檢查 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。

> [!Note]  
> 此函數不保證 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構有效，或使用結構的程式碼是安全的。

 

## <a name="syntax"></a>語法


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbmi* 
</dt> <dd>

要驗證之 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構的指標。

</dd> <dt>

*cbSize* 
</dt> <dd>

保存結構之記憶體區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回布林值。 如果值為 **FALSE**，則表示 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構無效。

## <a name="remarks"></a>備註

此函數會針對下列錯誤進行防護：

-   結構大小或無效結構大小的算術溢位。
-   **BiClrUsed** 成員的值無效。
-   影像大小的算術溢位 (**biSizeImage**) 。
-   針對 RGB 格式 (**biSizeImage**) 的影像大小值無效。

此函數不會檢查結構是否描述有效的影片格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Checkbmi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




