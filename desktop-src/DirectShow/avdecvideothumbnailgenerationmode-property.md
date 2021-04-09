---
description: 啟用或停用影片解碼中的縮圖產生模式。
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: 'AVDecVideoThumbnailGenerationMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935981"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>AVDecVideoThumbnailGenerationMode 屬性

啟用或停用影片解碼中的縮圖產生模式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>備註

如果值為 **VARIANT \_ TRUE**，則此解碼器會使用已優化的設定來快速產生縮圖影像。  (例如，它可能會略過 B 或 P 框架。 ) 否則，如果值為 **VARIANT \_ FALSE**，則會使用其一般解碼設定。

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

 

 




