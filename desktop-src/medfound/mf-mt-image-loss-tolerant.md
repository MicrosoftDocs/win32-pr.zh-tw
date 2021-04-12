---
description: 指定 ASF 影像資料流程是否為 degradable JPEG 類型。
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: 'MF_MT_IMAGE_LOSS_TOLERANT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848105"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>MF \_ MT \_ 影像 \_ 遺失 \_ 容錯屬性

指定 ASF 影像資料流程是否為 degradable JPEG 類型。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

此屬性適用于 ASF 中影像資料流程的媒體類型。 如果值為 **TRUE**，則資料流程是 degradable JPEG 影像類型。 否則，資料流程是 JFIF 影像類型。 如需這些資料流程類型的詳細資訊，請參閱 ASF 規格。

除了 MF \_ MT \_ 影像 \_ 遺失 \_ 容錯屬性之外，ASF 映射資料流程的媒體類型還包含下列屬性：



| 屬性                                                 | 描述                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) | 包含值 **MFMediaType \_ 影像**。 |
| [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md) | 提供影像大小（以圖元為單位）。            |



 

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




