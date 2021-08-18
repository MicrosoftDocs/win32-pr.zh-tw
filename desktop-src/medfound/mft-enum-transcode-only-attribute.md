---
description: 指定是否針對轉碼（而非播放）優化解碼器。
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: 'MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0951d4f370849678eb88ecbd9751c417a7e50d2bd709ad1f2c5b6cf96f5f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973077"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>\_ \_ \_ 僅限轉碼 \_ 屬性屬性的 MFT 列舉

指定是否針對轉碼（而非播放）優化解碼器。

目前，這個屬性只適用于使用 AVStream 迷你驅動程式的硬體型解碼器。 屬性會儲存在登錄中的解碼器功能資訊下。 如需詳細資訊，請參閱 [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey)的檔。

應用程式通常不會使用此屬性。

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

如果此登錄專案存在且等於1，則 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式會略過此解碼器，除非呼叫端在 **MFTEnumEx** 中指定了 [ **\_ \_ \_ \_ 僅轉碼**] 旗標。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
