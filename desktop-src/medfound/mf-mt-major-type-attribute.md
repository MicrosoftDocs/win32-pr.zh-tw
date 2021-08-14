---
description: 媒體類型的主要類型 GUID。
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: 'MF_MT_MAJOR_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98efe9d8ff86769faa8fecd911f80caa87e7266e60cf0c36c2850fe3c12922df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692243"
---
# <a name="mf_mt_major_type-attribute"></a>MF \_ MT \_ 主要 \_ 類型屬性

媒體類型的主要類型 GUID。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

主要類型會定義媒體資料的整體分類。 主要類型包括影片、音訊、腳本等等。 如需可能值的清單，請參閱 [主要媒體類型](media-type-guids.md)。

取得此屬性的替代方式是呼叫 [**IMFMediaType：： GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




