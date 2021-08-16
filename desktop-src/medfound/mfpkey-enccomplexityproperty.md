---
description: 指定編碼演算法的複雜度。
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: 'MFPKEY_ENCCOMPLEXITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93abe02b50f862fec706f75449e00643228a3917bc22ca9dafa9285d9d46be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690123"
---
# <a name="mfpkey_enccomplexity-property"></a>MFPKEY \_ ENCCOMPLEXITY 屬性

指定編碼演算法的複雜度。 值是介於0與100之間的整數，其中0指定最不復雜的演算法，而100則指定最複雜的演算法。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="default-value"></a>預設值

100適用于 Windows Media 音訊10和 Windows Media 音訊 10 Professional

100 Windows Vista 版本的 Windows Media 音訊10無損

0代表 Windows 7 版本 Windows Media 音訊10個無損

## <a name="remarks"></a>備註

如果 [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) 屬性的值為 **VARIANT \_ TRUE**，編碼器會根據此屬性的值來調整其演算法的複雜度。

針對 Windows Media 音訊10編碼器和 Windows Media 音訊 10 Professional 編碼器，如果此屬性的值為100，則編碼器會對 CPU 產生高需求，並產生最高品質的輸出。 當此屬性的值減少時，CPU 的需求會減少，但輸出品質也會減少。

針對 Windows Media 音訊10個無失真編碼器，如果此屬性的值為0，則編碼器會對 CPU 造成較低的需求。 當此屬性的值增加時，CPU 的需求會增加，而且編碼器輸出的大小會稍微減少。 無論這個屬性的值為何，輸出都不會失真。

如果您將此屬性保留為 **變數 \_ FALSE** 的預設值，則編碼器會使用它的預設演算法。 預設演算法取決於您所使用的編碼器，以及正在執行的 Windows 版本。 下表描述不同組合的預設行為。



| 作業系統 | 預設行為                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Windows Media 音訊10、Windows Media 音訊 10 Professional 以及 Windows Media 音訊10個無失真編碼器預設都使用最複雜的演算法。                                                    |
| Windows 7        | Windows Media 音訊10和 Windows Media 音訊 10 Professional 編碼器預設會使用最複雜的演算法。 Windows Media 音訊10個無失真編碼器預設會使用最不復雜的演算法。 |



 

如果 [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) 屬性的值為 **VARIANT \_ FALSE**，則編碼器會忽略這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
