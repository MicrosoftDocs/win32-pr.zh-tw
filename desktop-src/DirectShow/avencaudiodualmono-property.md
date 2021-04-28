---
description: AVEncAudioDualMono 屬性-指定雙聲道音訊是否編碼為身歷聲或雙 mono。
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: 'AVEncAudioDualMono 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096576"
---
# <a name="avencaudiodualmono-property"></a>AVEncAudioDualMono 屬性

指定雙聲道音訊是否編碼為身歷聲或雙 mono。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncAudioDualMono**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) 列舉的成員。

## <a name="remarks"></a>備註

此屬性不適用於 MPEG 音訊編碼器。 若為 MPEG 音訊，請使用 [**AVEncMPACodingMode**](avencmpacodingmode-property.md) 屬性。

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

 

