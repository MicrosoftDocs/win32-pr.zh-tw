---
description: 指定 AAC 解碼器是否使用標準的 MPEG-2/MPEG-4 身歷聲 downmix 方程式，或使用非標準的 downmix。
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: 'AVDecAACDownmixMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972316"
---
# <a name="avdecaacdownmixmode-property"></a>AVDecAACDownmixMode 屬性

指定 AAC 解碼器是否使用標準的 MPEG-2/MPEG-4 身歷聲 downmix 方程式，或使用非標準的 downmix。

非標準 downmix 的範例，是由 ARIB 檔 STD-B21 4.4 版所定義。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) 列舉的成員。

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

 

