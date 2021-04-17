---
description: 指定套用平均位元速率的時間間隔。 這個屬性會與 AVEncCommonMeanBitRate 屬性搭配使用。
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: 'AVEncCommonMeanBitRateInterval 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467892"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>AVEncCommonMeanBitRateInterval 屬性

指定套用平均位元速率的時間間隔。 這個屬性會與 [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) 屬性搭配使用。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT64** (**VT \_ UI8**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>屬性值

這個屬性具有線性範圍的值。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。

## <a name="remarks"></a>備註

針對兩個傳遞的變數位元速率 (VBR) 編碼方式，值為0表示時間間隔是內容的完整持續時間。 針對單一傳遞的常數速率 (CBR) 編碼方式，值為零表示編碼器選取的間隔 (通常是0.5 秒) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




