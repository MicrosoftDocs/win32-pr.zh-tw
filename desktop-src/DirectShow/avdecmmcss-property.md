---
description: 指定解碼執行緒的多媒體類別排程器服務 (MMCSS) 類別。
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: 'AVDecMmcss 屬性 (Uuid .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984851"
---
# <a name="avdecmmcss-property"></a>AVDecMmcss 屬性

指定解碼執行緒的多媒體類別排程器服務 (MMCSS) 類別。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**BSTR** (**VT \_ bstr**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>屬性值

這個屬性的值是 MMCSS 類別的名稱。

## <a name="remarks"></a>備註

MMCSS 可讓應用程式確保時間緊迫的處理已優先存取 CPU 資源。 其運作方式是將已註冊的執行緒提升為較高的執行緒優先順序，同時定期降低其優先順序，以產生時間給其他進程。

音訊解碼器的建議值為「音訊」，而影片解碼器的建議值為「播放」。

如果 MMCSS 服務無法使用，或指定的 MMCSS 類別不存在，則設定屬性不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Uuid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




