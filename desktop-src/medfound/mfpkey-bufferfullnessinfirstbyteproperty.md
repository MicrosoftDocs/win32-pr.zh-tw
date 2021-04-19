---
description: 指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: 'MFPKEY_BUFFERFULLNESSINFIRSTBYTE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001436"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE 屬性

指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="remarks"></a>備註

取得此值之前，您必須先設定輸出類型。

您可以使用 [IWMCodecProps：： GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)取得這個屬性的值。 如果您使用 **IPropertyBag**，您必須先使用 [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md) 屬性來設定所需壓縮格式的 FOURCC 值。

在所有主要畫面格的第一個位元組中具有緩衝區飽和度，可讓您在串連壓縮的影片串流時，判斷所需的緩衝區大小。

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

 

 




