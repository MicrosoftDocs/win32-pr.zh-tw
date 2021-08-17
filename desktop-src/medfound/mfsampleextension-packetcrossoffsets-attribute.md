---
description: 指定受保護範例框架中裝載界限的位移。
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: 'MFSampleExtension_PacketCrossOffsets 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39abdcaf0dfb5888c1705a0a76a19c3a55be522b82405f5a77345efe0d8f13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102304"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a>MFSampleExtension \_ PacketCrossOffsets 屬性

指定受保護範例框架中裝載界限的位移。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

此屬性適用于受 Windows 媒體數位 Rights Management (DRM) 保護的媒體範例。 屬性的值是 **DWORD** s 的陣列。 陣列中的每個專案都是裝載界限的位移（相對於框架的開頭）。 應用程式在解密和重建框架時可以使用這些值。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF 分隔器](asf-splitter.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 




