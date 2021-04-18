---
title: Windows Media 格式 SDK 結構
description: Windows Media 格式 SDK 結構
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Media Format SDK，結構
- Advanced Systems Format (ASF) 、結構
- ASF (Advanced Systems Format) ，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965464"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Media 格式 SDK 結構

Windows Media Format SDK 會執行下列結構。



| 結構                                                                                | Description                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM \_ 複製 \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | 保留適用于 DRM 授權中複製動作的輸出保護層級資訊。                                                                               |
| [**DRM \_ 授權 \_ 狀態 \_ 資料**](drm-license-state-data.md)                              | 包含有關指定之 [*DRM*](wmformat-glossary.md)許可權的 [*授權*](wmformat-glossary.md)資訊。 |
| [**DRM \_ 最小 \_ 輸出 \_ 保護 \_ 層級**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | 保存 DRM 授權所需的最小輸出保護層級，以各種格式播放內容。                                                                      |
| [**DRM \_ OPL \_ 輸出 \_ 識別碼**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | 保存 DRM 技術識別碼的陣列。 此結構是用來定義其他 DRM 結構中的技術群組。                                            |
| [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | 保留適用于 DRM 授權中「播放」動作的輸出保護層級資訊。                                                                               |
| [**DRM \_ 播放清單 \_ 內容 \_ 識別碼**](drm-playlist-content-id.md)                            | 包含要在播放清單燒錄過程中複製到 CD 的內容相關資訊。                                                                                 |
| [**DRM \_ VAL16**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | 儲存用來作為裝置識別碼的128位值。                                                                                                                       |
| [**DRM \_ 影片 \_ 輸出 \_ 保護**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | 保存影片保護技術的識別碼，以及該技術所需的設定資料。                                                             |
| [**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | 保存 **DRM \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | 定義波形音訊資料的格式。                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | 針對具有多個通道的格式，定義波形音訊資料的格式。                                                                                      |
| [**WM \_ 位址 \_ ACCESSENTRY**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | 指定 IP 位址存取清單中的專案。                                                                                                                          |
| [**WM \_ 用戶端 \_ 屬性**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | 記錄有關用戶端的資訊。                                                                                                                                     |
| [**WM \_ 用戶端 \_ 屬性， \_ 例如**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | 記錄有關用戶端的擴充資訊。                                                                                                                            |
| [**WM \_ 取得 \_ 授權 \_ 資料**](wm-get-license-data.md)                                    | 包含 DRM 授權的相關資訊。                                                                                                                                 |
| [**WM \_ 賦予 \_ 狀態**](wm-individualize-status.md)                             | 記錄 [*個人化*](wmformat-glossary.md) 流程的狀態。                                                                |
| [**WM \_ 有漏洞 \_ BUCKET \_ 組**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | 說明變數位元速率 (VBR) 檔的緩衝需求。                                                                                                  |
| [**WM \_ 授權 \_ 狀態 \_ 資料**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | 封裝 [**drm \_ 授權 \_ 狀態 \_ 資料**](drm-license-state-data.md) 結構，以描述 drm 授權狀態資料。                                              |
| [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | 描述媒體範例。                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | 描述 MPEG-2 影片串流。                                                                                                                                         |
| [**WM \_ 圖片**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | 包含 [**WM/圖片**](wmpicture.md) 複雜中繼資料屬性的資料。                                                                                     |
| [**WM \_ 埠 \_ 號碼 \_ 範圍**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | 描述 **IWMReaderNetworkConfig** 介面所使用之埠號碼的範圍。                                                                                     |
| [**WM \_ 讀取器 \_ CLIENTINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | 描述存取媒體串流 (播放機) 的用戶端讀取者。                                                                                                          |
| [**WM \_ 讀取器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | 描述讀取操作的效能。                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | 定義腳本資料流程的格式。                                                                                                                                    |
| [**WM \_ 串流 \_ 優先順序 \_ 記錄**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | 包含資料流程號碼，並指定該資料流程的傳遞是否為強制性。                                                                                      |
| [**WM \_ 資料流程 \_ 類型 \_ 資訊**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | 包含 [**WM/StreamTypeInfo**](wm-streamtypeinfo.md) 複雜中繼資料屬性的資料。                                                                      |
| [**WM \_ 內容 \_ 歌詞**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | 包含 [**WM/歌詞 \_ 內容**](wm-lyrics-synchronised.md) 複雜中繼資料屬性的資料。                                                           |
| [**WM \_ 使用者 \_ 文字**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | 包含 [**WM/Text**](wm-text.md) 複雜中繼資料屬性的資料。                                                                                          |
| [**WM \_ 使用者 \_ WEB \_ URL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | 包含 [**WM/UserWebURL**](wm-userweburl.md) 複雜中繼資料屬性的資料。                                                                              |
| [**WM \_ 寫入器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | 描述寫入作業的效能。                                                                                                                         |
| [**WM \_ 寫入器 \_ 統計資料， \_ 例如**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | 包含擴充寫入器統計資料。                                                                                                                                      |
| [**WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰**](wmdrm-import-content-key.md)                          | 保存匯入受保護內容時所使用的內容金鑰。                                                                                                                |
| [**WMDRM 匯 \_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | 保存用來匯入受保護內容的加密工作階段金鑰和內容金鑰。                                                                                      |
| [**WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰**](wmdrm-import-session-key.md)                          | 保存工作階段金鑰以匯入受保護的內容。                                                                                                                    |
| [**WMT \_ 緩衝區 \_ 區段**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | 包含在封包中指定區段所需的資訊。                                                                                                      |
| [**WMT \_ COLORSPACEINFO \_ 延伸模組 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | 包含 WM \_ SampleExtensionGUID \_ ColorSpaceInfo 資料單位延伸模組的資料。                                                                                    |
| [**WMT \_ FILESINK \_ 資料 \_ 單位**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | 包含封包的相關資訊。                                                                                                                                      |
| [**WMT \_ 裝載 \_ 片段**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | 包含從封包解壓縮裝載片段所需的資訊。                                                                                           |
| [**WMT 時間 \_ 碼 \_ 延伸 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | 包含單一 SMPTE 時間碼和相關資訊。                                                                                                                |
| [**WMT \_ VIDEOIMAGE \_ 範例**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | 包含影片影像範例的相關資訊。                                                                                                                          |
| [**WMT \_ 水位線 \_ 專案**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | 包含浮水印系統的相關資訊。                                                                                                                         |
| [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | 包含 Web 資料流程的相關資訊。                                                                                                                                  |
| [**WMT \_ WEBSTREAM \_ 範例 \_ 標頭**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | 包含 Web 資料流程範例的標頭資訊。                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | 描述影片影像的點陣圖和色彩資訊。                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | 描述影片影像的點陣圖和色彩資訊，包括 [*交錯*](wmformat-glossary.md)、禁止複製和外觀比例。       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 
