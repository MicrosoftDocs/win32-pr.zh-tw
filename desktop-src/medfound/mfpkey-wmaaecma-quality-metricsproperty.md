---
description: 從語音捕捉 DSP (AEC) ，抓取聲場回應取消的品質計量。
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: 'MFPKEY_WMAAECMA_QUALITY_METRICS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977807"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>MFPKEY \_ WMAAECMA \_ 品質 \_ 計量屬性

從語音捕捉 DSP (AEC) ，抓取聲場回應取消的品質計量。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BLOB

## <a name="remarks"></a>備註

這個屬性的值是 [AecQualityMetrics \_ 結構](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) 結構。 這是唯讀的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
