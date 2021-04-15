---
description: 停止目前的編碼階段，或查詢目前的編碼傳遞是否為最後一次。
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: 'AVEncCommonPassEnd 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467890"
---
# <a name="avenccommonpassend-property"></a>AVEncCommonPassEnd 屬性

停止目前的編碼階段，或查詢目前的編碼傳遞是否為最後一次。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>備註

將此屬性設定為 **VARIANT \_ TRUE** 會結束目前的編碼傳遞。 將這個屬性設定為 **VARIANT \_ FALSE** 會終止 multipass 編碼。

讀取此屬性會查詢目前的編碼傳遞是否為最後一次。

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

 

 




