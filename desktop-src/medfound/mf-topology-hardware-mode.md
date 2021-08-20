---
description: 指定是否要載入以硬體為基礎的 Microsoft 媒體基礎轉換 (拓撲中的 MFTs) 。
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: 'MF_TOPOLOGY_HARDWARE_MODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52da08dc1da36072f02627ec632bb8caf189c1748545c1ded5c3e4ebdedc1234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875665"
---
# <a name="mf_topology_hardware_mode-attribute"></a>MF \_ 拓撲 \_ 硬體 \_ 模式屬性

指定是否要載入以硬體為基礎的 Microsoft 媒體基礎轉換 (拓撲中的 MFTs) 。

## <a name="data-type"></a>資料類型

**[**MFTOPOLOGY \_以 \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** **UINT32** 形式儲存的硬體模式

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

此屬性是選擇性的。 在解析拓撲之前，請先設定屬性。



| 值                                  | 描述                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ 使用 \_ 硬體**  | 拓撲載入器會載入以硬體為基礎的 MFTs，例如硬體解碼器（如果有的話）。<br/> 如果找不到硬體解碼器，或硬體解碼器因為某些原因而無法連線，拓撲載入器會自動切換回軟體解碼。<br/> |
| **\_ \_ 僅限 MFTOPOLOGY HWMODE SOFTWARE \_** | 拓撲載入器只會載入軟體 MFTs，包括軟體解碼器。                                                                                                                                                                                                    |



 

預設值為 **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_**，以與現有的應用程式相容。 建議的值為 **MFTOPOLOGY \_ HWMODE \_ USE \_ 硬體**。

如果拓撲載入器將硬體 MFT 插入拓撲中，它會在 [拓撲] 節點上設定 [ [mft \_ 列舉 \_ 硬體 \_ URL] \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性。 若要檢查硬體 MFT 是否存在，請列舉已解析拓撲中的節點，並檢查此屬性是否存在。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




