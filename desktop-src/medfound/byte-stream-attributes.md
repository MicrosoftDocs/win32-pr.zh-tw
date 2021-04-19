---
description: 位元組資料流程屬性
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: 位元組資料流程屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000054"
---
# <a name="byte-stream-attributes"></a>位元組資料流程屬性

下列屬性適用于某些位元組資料流程。 若要找出位元組資料流程是否支援屬性，請查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的位元組資料流程物件。



| 屬性                                                                                  | 描述                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**MF \_ BYTESTREAM \_ 內容 \_ 類型**](mf-bytestream-content-type-attribute.md)              | 指定位元組資料流程的 MIME 類型。                         |
| [**MF \_ BYTESTREAM \_ 持續期間**](mf-bytestream-duration-attribute.md)                       | 指定位元組資料流程的持續時間，以 100-毫微秒單位表示。 |
| [MF \_ BYTESTREAM \_ IFO \_ 檔案 \_ URI](mf-bytestream-ifo-file-uri.md)                           | 指定相關聯 IFO 檔案的 URL。                      |
| [**MF \_ BYTESTREAM \_ 上次 \_ 修改 \_ 時間**](mf-bytestream-last-modified-time-attribute.md) | 指定上一次修改位元組資料流程的時間。                   |
| [**MF \_ BYTESTREAM \_ 來源 \_ 名稱**](mf-bytestream-origin-name-attribute.md)                | 指定位元組資料流程的原始 URL。                     |



 

下列屬性適用于位元組資料流程處理常式。



| 屬性                                                                                    | 描述                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ 接受 \_ 共用 \_ 寫入](mf-bytestreamhandler-accepts-share-write.md) | 指定位元組資料流程處理常式是否可以使用開啟的位元組資料流程以供另一個執行緒寫入 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 



