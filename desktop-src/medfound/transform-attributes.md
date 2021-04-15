---
description: 轉換屬性
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: 轉換屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469256"
---
# <a name="transform-attributes"></a>轉換屬性

下列屬性適用于 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) ，或適用于 MFTs 的 [啟用物件](activation-objects.md) 或兩者。



| 屬性                                                                                                     | 描述                                                                                                                                                                                   | 套用至                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**已 \_ 鎖定 MF 啟用 \_ MFT \_**](mf-activate-mft-locked-attribute.md)                                         | 指定拓撲載入器是否會變更 MFT 上的媒體類型。                                                                                                                  | MFTs                        |
| [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)                                                       | 指定媒體基礎轉換 (MFT) 是否支援 DirectX Video 加速。                                                                                                     | MFTs                        |
| [MF \_ 轉換 \_ 非同步](mf-transform-async.md)                                                                | 指定 MFT 是否執行非同步處理。                                                                                                                                    | MFTs                        |
| [MF \_ 轉換 \_ 非同步 \_ 解除鎖定](mf-transform-async-unlock.md)                                                 | 啟用非同步 MFT 的使用。                                                                                                                                                       | MFTs                        |
| [MF \_ 轉換 \_ 類別目錄 \_ 屬性](mf-transform-category-attribute.md)                                     | 指定 MFT 的分類。                                                                                                                                                            | MFT 啟用物件      |
| [MF \_ 轉換 \_ 旗標 \_ 屬性](mf-transform-flags-attribute.md)                                           | 包含 MFT 啟用物件的旗標。                                                                                                                                                  | MFT 啟用物件      |
| [MFT \_ 編解碼器的 \_ 業績 \_ 屬性](mft-codec-merit-attribute.md)                                                 | 包含硬體編解碼器的業績值。                                                                                                                                                 | MFT 啟用物件      |
| [MFT \_ 連接的 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md)                                       | 包含以硬體為基礎的 MFT 上連接資料流程的資料流程屬性指標。                                                                                                  | MFTs                        |
| [\_連接 \_ 至 \_ HW \_ 串流的 MFT](mft-connected-to-hw-stream.md)                                              | 指定以硬體為基礎的 MFT 是否已連接到另一個以硬體為基礎的 MFT。                                                                                                            | MFTs                        |
| [MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序公開輸出類型](mft-decoder-expose-output-types-in-native-order.md) | 指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。                                                                                   | MFTs                        |
| [MFT \_ 解碼 \_ 最後 \_ 影片 \_ 解析度 \_ 提示](mft-decoder-final-video-resolution-hint.md)                   | 指定在視頻處理之後，解碼影像的最終輸出解析度。                                                                                                           | MFTs                        |
| [MFT \_ 編碼器 \_ 支援 \_ CONFIG \_ 事件](mft-encoder-supports-config-event.md)                                | 指定在串流處理時，MFT 編碼器支援接收 [MEEncodingParameter](meencodingparameters.md) 事件。                                                                     | MFTs                        |
| [MFT \_ 列舉 \_ 介面卡 \_ LUID](mft-enum-adapter-luid.md)                                                         | 指定視訊卡的唯一識別碼。 呼叫 MFTEnum2 時，請使用這個屬性來列舉與特定介面卡相關聯的 MFTs。                                             | MFTs                        |
| [MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md)                                    | 包含以硬體為基礎的 MFT 的符號連結。                                                                                                                                          | MFTs/MFT 啟用物件 |
| [MFT \_ 列舉 \_ 硬體 \_ 廠商 \_ 識別碼 \_ 屬性](mft-enum-hardware-vendor-id-attribute.md)                       | 指定以硬體為基礎的媒體基礎轉換的廠商識別碼                                                                                                                       | MFTs                        |
| [\_ \_ 僅限 MFT 列舉轉碼 \_ \_ 屬性](mft-enum-transcode-only-attribute.md)                                | 指定是否針對轉碼（而非播放）優化解碼器。                                                                                                            | MFTs                        |
| [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)                                     | 包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，可用來解除鎖定 MFT。                                                                            | MFT 啟用物件      |
| [MFT \_ 易記 \_ 名稱 \_ 屬性](mft-friendly-name-attribute.md)                                             | 包含以硬體為基礎的 MFT 的顯示名稱。                                                                                                                                           | MFT 啟用物件      |
| [MFT \_ 輸入 \_ 類型 \_ 屬性](mft-input-types-attributes.md)                                               | 包含已註冊的 MFT 輸入類型。                                                                                                                                               | MFT 啟用物件      |
| [MFT \_ 輸出 \_ 類型 \_ 屬性](mft-output-types-attributes.md)                                             | 包含對 MFT 註冊的輸出類型。                                                                                                                                              | MFT 啟用物件      |
| [MFT \_ 慣用 \_ 編碼器 \_ 設定檔](mft-preferred-encoder-profile.md)                                         | 包含編碼器的設定屬性。                                                                                                                                             | MFT 啟用物件      |
| [MFT \_ 慣用 \_ OUTPUTTYPE \_ 屬性](mft-preferred-outputtype-attribute.md)                               | 指定編碼器慣用的輸出格式。                                                                                                                                         | MFT 啟用物件      |
| [MFT \_ 慣用 \_ OUTPUTTYPE \_ 屬性](mft-preferred-outputtype-attribute.md)                               | 指定編碼器慣用的輸出格式。                                                                                                                                         | MFT 啟用物件      |
| [MFT \_ 進程 \_ 區域 \_ 屬性](mft-process-local-attribute.md)                                             | 指定是否僅在應用程式的進程中註冊 MFT。                                                                                                                     | MFT 啟用物件      |
| [MFT \_ REMUX \_ 將 \_ 我 \_ 的圖片標示 \_ 為 \_ 乾淨 \_ 點](mft-remux-mark-i-picture-as-clean-point.md)                 | 指定 h.264 video remux MFT 是否應將圖片標示為乾淨點，以取得更好的搜尋能力。 這可能會在搜尋不符合規範的最終將檔案中進行搜尋。 | MFT 啟用物件      |
| [MFT \_ 支援 \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | 指定媒體基礎轉換 (MFT) 是否支援 3D stereoscopic 影片。                                                                                                          | MFT 啟用物件      |
| [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md)                  | 指定媒體基礎轉換 (MFT) 是否支援動態格式變更。                                                                                                         | MFTs                        |
| [MFT \_ 轉換 \_ CLSID \_ 屬性](mft-transform-clsid-attribute.md)                                         | 包含 MFT (CLSID) 的類別識別碼。                                                                                                                                              | MFT 啟用物件      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 



