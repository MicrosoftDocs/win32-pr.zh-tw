---
description: SetClipVideoRect 方法會將影片顯示星號調整至指定的 subrectangle。
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: SetClipVideoRect 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7741a2604ed1c2896b105295020893e23b447e3fa6f6ab7c53def92aa508c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078868"
---
# <a name="setclipvideorect-method"></a>SetClipVideoRect 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

方法會將 `SetClipVideoRect` 影片顯示星號調整至指定的 subrectangle。

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

指定包含裁剪矩形的 [DVDRect](dvdrect-object.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

當您設定新的裁剪矩形時，物件會將該區域放大，以符合應用程式的整體顯示尺寸。 這會在螢幕的特定區域中建立效果放大。 若要指定矩形，請建立新的 [DVDRect](dvdrect-object.md) 物件並填入其屬性。

影片顯示最常見的矩形是 720 x 540。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



