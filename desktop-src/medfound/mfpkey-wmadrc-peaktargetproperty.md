---
description: 指定輸出音訊內容所需的最大音量層級。
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: 'MFPKEY_WMADRC_PEAKTARGET 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974209"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>MFPKEY \_ WMADRC \_ PEAKTARGET 屬性

指定輸出音訊內容所需的最大音量層級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

請參閱＜備註＞。

## <a name="remarks"></a>備註

您可以針對動態範圍控制項的目的，在解碼器上設定此值，但只有在已設定 [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) 屬性時，才會有作用。

如果您在未設定此屬性時，從編碼器要求動態範圍控制，則編解碼器會計算預設值。

您可以使用 [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) 和 [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) 屬性來計算這個屬性的適當值。

如需動態範圍控制的詳細資訊，請參閱 web 文章 [Windows Media 音訊 Professional 編解碼器功能](/previous-versions/ms867218(v=msdn.10))。

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

 

 
