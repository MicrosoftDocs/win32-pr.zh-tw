---
description: 接收寫入器屬性
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: 接收寫入器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114353"
---
# <a name="sink-writer-attributes"></a>接收寫入器屬性

您可以使用下列屬性來初始化接收寫入器。



| 屬性                                                                                  | 描述                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ 低 \_ 延遲](mf-low-latency.md)                                                     | 啟用低延遲處理。                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ 停用 \_ 轉換器](mf-readwrite-disable-converters.md)                  | 啟用或停用接收寫入器的格式轉換。                                                                                                                                                                         |
| [MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換](mf-readwrite-enable-hardware-transforms.md) | 可讓接收寫入器使用以硬體為基礎的媒體基礎轉換 (MFTs) 。                                                                                                                                                  |
| [MF \_ 接收 \_ 寫入器 \_ 非同步 \_ 回呼](mf-sink-writer-async-callback.md)                     | 包含接收器寫入器的應用程式回呼介面指標。                                                                                                                                                    |
| [MF \_ 接收 \_ 寫入器 \_ 停用 \_ 節流](mf-sink-writer-disable-throttling.md)             | 指定接收寫入器是否限制傳入資料的速率。                                                                                                                                                                |
| [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md)                             | 指定輸出檔的容器類型。                                                                                                                                                                                   |
| [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)                  | 包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，用來將具有使用規定限制的 MFT 解除鎖定。 如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。 |
| [MF \_ 接收 \_ 寫入器 \_ D3D \_ 管理員](mf-sink-writer-d3d-manager.md)                           | 使用此屬性可為接收寫入器載入的任何影片編碼器或媒體接收器提供 Direct3D 裝置。                                                                                                                   |



 

使用這些屬性搭配下列方法和函數：

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

若要使用這些屬性的任何一項，請先呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。 然後使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，在屬性存放區上設定所需的屬性。 將 **IMFAttributes** 指標傳遞至先前所列之任何方法或函數的 *pAttributes* 參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 



