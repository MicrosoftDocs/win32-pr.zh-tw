---
description: 指定語音捕獲 DSP 是否套用麥克風增益區。
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: 'MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d00e906ec953e2fd00d9c288336c322c2d0dc07ea1c2d74a014ab78ae21acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113148"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>MFPKEY \_ WMAAECMA \_ MIC \_ 增益 \_ BOUNDER 屬性

指定語音捕獲 DSP 是否套用麥克風增益區。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ TRUE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

麥克風增益界限可確保麥克風具有正確的增益等級。 如果增益過高，則捕捉的信號可能會飽和，並會被裁剪。 裁剪是非線性效果，這會導致聲場回顯取消 (AEC) 演算法失敗。 如果增益過低，則信號雜訊比例很低，這也會導致 AEC 演算法失敗或無法正常執行。

這個屬性可以具有下列值。



| 值          | 描述                       |
|----------------|-----------------------------------|
| VARIANT \_ TRUE  | 啟用麥克風增益範圍。  |
| VARIANT \_ FALSE | 停用麥克風增益範圍。 |



 

這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。

只有在 DSP 以來源模式運作時，才會套用麥克風增益界限。 在篩選模式中，應用程式必須確定麥克風具有正確的增益等級。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
