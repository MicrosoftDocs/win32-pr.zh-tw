---
description: 指定您想要用於影片編碼的裝置一致性範本。
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: 'MFPKEY_DECODERCOMPLEXITYREQUESTED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980799"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>MFPKEY \_ DECODERCOMPLEXITYREQUESTED 屬性

指定您想要用於影片編碼的裝置一致性範本。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

1

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCDecoderComplexityRequested

## <a name="data-type-for-ipropertybag"></a>IPropertyBag 的資料類型

VT \_ BSTR

## <a name="default-value-for-ipropertybag"></a>IPropertyBag 的預設值

多功能

## <a name="remarks"></a>備註

編解碼器將嘗試使用此值指定的裝置一致性範本來編碼內容。 編碼之後，您可以從 [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) 屬性中取出編碼內容符合的實際範本。

這個屬性必須是下列其中一個值。



| IPropertyStore 的值 | IPropertyBag 的值 | 描述         |
|--------------------------|------------------------|---------------------|
| 0                        | SP-1                   | 簡單設定檔      |
| 1                        | 多功能                   | 主要設定檔        |
| 2                        | CP                   | 不再支援 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




