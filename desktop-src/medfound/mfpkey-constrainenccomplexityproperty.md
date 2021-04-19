---
description: 指定是否限制音訊編碼演算法的複雜度。
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: 'MFPKEY_CONSTRAINENCOMPLEXITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997519"
---
# <a name="mfpkey_constrainencomplexity-property"></a>MFPKEY \_ CONSTRAINENCOMPLEXITY 屬性

指定是否限制音訊編碼演算法的複雜度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

如果您將此屬性保留為預設值 [ **VARIANT \_ FALSE**]，則音訊編碼器會使用它的預設演算法。 預設演算法取決於輸出類型以及正在執行的 Windows 版本。 下表描述不同組合的預設行為。



| 作業系統 | 預設行為                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | 針對所有輸出類型，音訊編碼器預設會使用最複雜的演算法。                                                                                                                 |
| Windows 7        | 針對標準和專業輸出類型，音訊編碼器預設會使用最複雜的演算法。 針對無損輸出類型，音訊編碼器預設會使用最不復雜的演算法。 |



 

如果您將此屬性設定為 **VARIANT \_ TRUE**，您也必須藉由設定 [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) 屬性來指定複雜度值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
