---
description: 指定編碼器是否使用變數位速率 (VBR) 編碼。
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: 'MFPKEY_VBRENABLED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848796"
---
# <a name="mfpkey_vbrenabled-property"></a>MFPKEY \_ VBRENABLED 屬性

指定編碼器是否使用變數位速率 (VBR) 編碼。 讀寫。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

**g \_ wszWMVCVBREnabled**、 **g \_ wszWMCPAudioVBRSupported**

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

針對編解碼器所使用的任何其他 VBR 屬性，此值必須設定為 **VARIANT \_ TRUE** 。

當您在音訊編碼器上將此值設定為 **VARIANT \_ TRUE** 之後，使用 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) 方法取出的輸出類型就是 VBR 類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MFPKEY \_ 限制 \_ 列舉 \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**MFPKEY \_ 所需的 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
