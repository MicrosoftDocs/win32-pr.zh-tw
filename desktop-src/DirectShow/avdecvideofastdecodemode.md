---
description: 取得或設定影片解碼速度。
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: 'AVDecVideoFastDecodeMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109677"
---
# <a name="avdecvideofastdecodemode-property"></a>AVDecVideoFastDecodeMode 屬性

取得或設定影片解碼速度。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>屬性值

這個屬性的值範圍從0到32，其中0表示正常解碼，而32是最快速的解碼模式。 確切的行為取決於解碼器的執行。 並非1和32之間的每個增量都必須定義為不同的模式。

[**EAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)列舉包含這個屬性的一些預先定義模式。

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

 

 




