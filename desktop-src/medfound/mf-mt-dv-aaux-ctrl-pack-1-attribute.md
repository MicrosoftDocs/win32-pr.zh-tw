---
description: 音訊輔助 (AAUX 數位視訊中第二個音訊區塊的) 原始檔控制套件 (DV) 媒體類型。
ms.assetid: e9c17940-beb7-4034-95a3-983aaca0c905
title: 'MF_MT_DV_AAUX_CTRL_PACK_1 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119c58d6a988f955229b46c0cb482bc24dd6f770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985174"
---
# <a name="mf_mt_dv_aaux_ctrl_pack_1-attribute"></a>MF \_ MT \_ DV \_ AAUX \_ CTRL \_ PACK \_ 1 屬性

音訊輔助 (AAUX 數位視訊中第二個音訊區塊的) 原始檔控制套件 (DV) 媒體類型。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會對應至 DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo)結構的 **dwDVAAuxCtl1** 成員。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 
