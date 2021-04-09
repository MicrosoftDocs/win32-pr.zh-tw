---
description: 指定編碼器支援的編碼傳遞數目。
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: 'AVEncCommonMultipassMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846668"
---
# <a name="avenccommonmultipassmode-property"></a>AVEncCommonMultipassMode 屬性

指定編碼器支援的編碼傳遞數目。

這是唯讀的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>屬性值

這個屬性會以值範圍的形式傳回。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。

## <a name="remarks"></a>備註

解碼延遲會定義為必須緩衝的資料量。 例如，在 MPEG 影片編碼器上將此屬性設定為 **VARIANT \_ TRUE** 會限制編碼器可使用的 GOP 結構類型。

若要設定目前的編碼階段，請設定 [**AVEncCommonPassStart**](avenccommonpassstart-property.md) 屬性。

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

 

 




