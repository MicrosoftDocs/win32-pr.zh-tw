---
description: 包含以硬體為基礎的媒體基礎轉換 (MFT) 上連接資料流程的資料流程屬性指標。
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: 'MFT_CONNECTED_STREAM_ATTRIBUTE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848713"
---
# <a name="mft_connected_stream_attribute-attribute"></a>MFT \_ 連接的 \_ 資料流程 \_ 屬性屬性

包含以硬體為基礎的媒體基礎轉換 (MFT) 上連接資料流程的資料流程屬性指標。

## <a name="data-type"></a>資料類型

**IMFAttributes \** _ 儲存為 _*IUnknown \**_

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

應用程式通常不會使用此屬性。

這個屬性會用於作為硬體裝置之 proxy 的 MFTs。 如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[\_連接 \_ 至 \_ HW \_ 串流的 MFT](mft-connected-to-hw-stream.md)
</dt> <dt>

[硬體 MFTs](hardware-mfts.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




