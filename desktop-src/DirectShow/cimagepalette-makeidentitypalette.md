---
description: MakeIdentityPalette 方法會嘗試建立 &\# 0034; 身分識別選擇區 &\# 0034; 定義為直接對應至顯示裝置中所選取之調色板的識別碼。
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: 'CImagePalette. MakeIdentityPalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb6e9a4e2c6adc411b7b043e35dc6dacf45dbb6a6ee4cf326a1c1953c559c16f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916128"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>CImagePalette. MakeIdentityPalette 方法

方法會嘗試將「身分識別選擇區」 `MakeIdentityPalette` 定義為直接對應至顯示裝置中所選取之調色板的元件。

## <a name="syntax"></a>語法


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pEntry* 
</dt> <dd>

元件專案陣列的指標。

</dd> <dt>

*iColours* 
</dt> <dd>

*PEntry* 中的調色板專案數目。

</dd> <dt>

*szDevice* 
</dt> <dd>

字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。 若要使用主顯示器裝置，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 s OK \_ ，如果失敗，則傳回 FALSE。

## <a name="remarks"></a>備註

這個方法會比較系統元件中的保留專案與 *pEntry* 陣列中的對應專案。 如果它們完全相符，則方法會 \_ 在 *pEntry* 的其餘 (非保留) 的調色板專案中，設定電腦 NOCOLLAPSE 旗標。 此旗標會防止 GDI 嘗試將邏輯調色板專案對應至系統元件專案。

[**CImagePalette：： MakePalette**](cimagepalette-makepalette.md)方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




