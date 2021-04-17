---
description: 指定解碼器是否在有遺漏參考框架的框架內卸載。
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: 'AVDecVideoDropPicWithMissingRef 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187453"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>AVDecVideoDropPicWithMissingRef 屬性

指定解碼器是否在有遺漏參考框架的框架內卸載。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>備註

如果位流損毀，框架可能會遺失參考框架。 如果這個屬性的值為 **VARIANT \_ TRUE**，則此解碼器會卸載框架。 如果此值為 **VARIANT \_ FALSE**，則會嘗試使用一或多個附近的框架做為參考框架來解碼框架。 產生的已解碼框架將會有封鎖構件。

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

 

 




