---
title: 系統設定檔
description: 系統設定檔
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Media Format SDK，系統設定檔
- Advanced Systems Format (ASF) 、系統設定檔
- ASF (Advanced 系統格式) 、系統設定檔
- Windows Media 格式 SDK，設定檔識別碼
- Advanced Systems Format (ASF) ，設定檔識別碼
- ASF (Advanced 系統格式) ，設定檔識別碼
- 系統設定檔，清單
- 設定檔識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeca66023e6de6aba9c07a6bcb84a73756e316a8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681430"
---
# <a name="system-profiles"></a>系統設定檔

下表包含所支援系統設定檔的完整清單。 每個列出的設定檔都有一個名稱和一個設定檔識別碼。 設定檔識別碼是指派給系統設定檔的 GUID 值的常數集合。 若要在您的程式碼中使用系統設定檔識別碼，您必須在應用程式中包含 wmsysprf。 如需顯示如何載入系統設定檔的範例，請參閱 [載入系統設定檔](to-load-a-system-profile.md)。

> [!IMPORTANT]
> 以下列出的設定檔全都使用第8版 Windows Media 音訊和 Windows Media 視訊編解碼器。 沒有任何預先定義的系統設定檔使用 Windows Media 9 系列編解碼器。 您可以使用第8版的設定檔做為起點，建立自己的 Windows Media 9 系列設定檔。 如需詳細資訊，請參閱 [重複使用串流](reusing-stream-configurations.md)設定。

 



| 設定檔名稱                                                                      | 設定檔識別碼                     | Description                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media 視訊8適用于彩色 Pocket Pc (225 Kbps)                              | WMProfile \_ V80 \_ 255VideoPDA    | 建立影片檔案以在更快的彩色 Pocket Pc 上播放時，請使用此設定檔。                                                                                 |
| Windows Media 視訊8適用于彩色 Pocket Pc (150 Kbps)                              | WMProfile \_ V80 \_ 150VideoPDA    | 建立影片檔案以在大部分 Pocket Pc 上播放時，請使用此設定檔。                                                                                         |
| 撥號數據機的 Windows Media 視訊8或單一通道 ISDN (28.8 到 56 Kbps)  | WMProfile \_ V80 \_ 28856VideoMBR  | 針對具有撥號數據機或單一通道 ISDN 連接的目標物件，使用此多位元率設定檔 (頻寬介於 28.8 Kbps 到 56 Kbps 之間) 。        |
| Windows Media 視訊8適用于 LAN、纜線數據機或 xDSL (100 到 768 Kbps)              | WMProfile \_ V80 \_ 100768VideoMBR | 針對具有雙重通道 ISDN、LAN、纜線數據機或 xDSL 連線的目標物件，使用此多位元率設定檔 (頻寬介於 100 Kbps 到 500 Kbps 之間) 。 |
| 撥號數據機或 LAN (28.8 到 100 Kbps 的 Windows Media 視訊 8)                 | WMProfile \_ V80 \_ 288100VideoMBR | 針對具有撥號數據機、LAN 或雙通道 ISDN 連接的目標物件，使用此多位元率設定檔 (頻寬介於28.8 到 100 Kbps 之間) 。         |
| 撥號數據機的 Windows Media 視訊 8 (28.8 Kbps)                               | WMProfile \_ V80 \_ 288Video       | 將此設定檔用於低位速率音訊/影片傳遞超過 28.8 Kbps 的撥號連線。                                                                          |
| 撥號數據機的 Windows Media 視訊 8 (56 Kbps)                                 | WMProfile \_ V80 \_ 56Video        | 將此設定檔用於低位速率音訊/影片傳遞超過 56 Kbps 的撥號連線。                                                                            |
| 區域網路的 Windows Media 視訊 8 (100 Kbps)                            | WMProfile \_ V80 \_ 100Video       | 使用此設定檔可透過雙通道 ISDN、LAN 或纜線數據機連線來提供中位速率的傳遞。                                                              |
| 區域網路的 Windows Media 視訊 8 (256 Kbps)                            | WMProfile \_ V80 \_ 256Video       | 將此設定檔用於適用于本機播放或下載和播放的高品質音訊/影片內容。                                                     |
| 區域網路的 Windows Media 視訊 8 (384 Kbps)                            | WMProfile \_ V80 \_ 384Video       | 將此設定檔用於適用于本機播放或下載和播放的高品質音訊/影片內容。                                                     |
| 區域網路的 Windows Media 視訊 8 (768 Kbps)                            | WMProfile \_ V80 \_ 768Video       | 將此設定檔用於適用于本機播放或下載和播放的高品質音訊/影片內容。                                                     |
| 適用于寬頻 (NTSC Windows Media 視訊8，700 Kbps)                               | WMProfile \_ V80 \_ 700NTSCVideo   | 將此設定檔用於適用于本機播放或下載及播放的高品質音訊/影片內容。                                                         |
| 適用于寬頻 (NTSC Windows Media 視訊8，1400 Kbps)                              | WMProfile \_ V80 \_ 1400NTSCVideo  | 將此設定檔用於適用于本機播放或下載和播放的高品質音訊/影片內容。                                                     |
| 適用于寬頻 (PAL Windows Media 視訊8，384 Kbps)                                | WMProfile \_ V80 \_ 384PALVideo    | 將此設定檔用於適用于本機播放或下載和播放的高品質音訊/影片內容。                                                     |
| 適用于寬頻 (PAL Windows Media 視訊8，700 Kbps)                                | WMProfile \_ V80 \_ 700PALVideo    | 將此設定檔用於適用于本機播放或下載和播放的高品質音訊/影片內容。                                                     |
| 適用于撥號數據機的 Windows Media 音訊 8 (Mono、28.8 Kbps)                          | WMProfile \_ V80 \_ 288MonoAudio   | 將此設定檔用於電臺和音樂內容 (僅限音訊) 。                                                                                                          |
| 適用于撥號數據機的 Windows Media 音訊 8 (FM 無線電身歷聲，28.8 Kbps)               | WMProfile \_ V80 \_ 288StereoAudio | 將此設定檔用於電臺和音樂內容 (僅限音訊) 。                                                                                                          |
| 撥號數據機的 Windows Media 音訊 8 (32 Kbps)                                  | WMProfile \_ V80 \_ 32StereoAudio  | 將此設定檔用於電臺和音樂內容 (僅限音訊) 。                                                                                                          |
| 撥號數據機的 Windows Media 音訊 8 (接近 CD 品質，48 Kbps)                 | WMProfile \_ V80 \_ 48StereoAudio  | 用於收音機、音樂和一般用途的音訊內容。                                                                                                            |
| 適用于撥號數據機的 Windows Media 音訊 8 (CD 品質，64 Kbps)                      | WMProfile \_ V80 \_ 64StereoAudio  | 將此設定檔用於具有高速網際網路或 LAN 連接的目標物件。                                                                                  |
| Windows Media 音訊8適用于 ISDN (優於 CD 品質，96 Kbps)                   | WMProfile \_ V80 \_ 96StereoAudio  | 將此設定檔用於具有高速網際網路或 LAN 連接的目標物件。                                                                                  |
| Windows Media 音訊8適用于 ISDN (優於 CD 品質，128 Kbps)                  | WMProfile \_ V80 \_ 128StereoAudio | 將此設定檔用於具有高速網際網路或 LAN 連接的目標物件。                                                                                  |
| 撥號數據機的 Windows Media 視訊 8 (沒有音訊、28.8 Kbps)                      | WMProfile \_ V80 \_ 288VideoOnly   | 針對具有撥號數據機的目標物件建立僅供影片使用的內容時，請使用此設定檔。                                                                         |
| 撥號數據機的 Windows Media 視訊 8 (沒有音訊、56 Kbps)                        | WMProfile \_ V80 \_ 56VideoOnly    | 針對具有撥號數據機的目標物件建立僅供影片使用的內容時，請使用此設定檔。                                                                         |
| 適用于寬頻的 Windows Media 8 公平品質型 VBR                              | WMProfile \_ V80 \_ FAIRVBRVideo   | 適用于品質受限的 VBR 內容，公平到高品質的設定檔。                                                                                     |
| 適用于寬頻的 Windows Media 8 高品質基礎 VBR。                             | WMProfile \_ V80 \_ HIGHVBRVideo   | 針對品質受限的 VBR 內容，提供高品質的最優質基礎設定檔。                                                                                     |
| 適用于寬頻的 Windows Media 8 最佳品質型 VBR。                             | WMProfile \_ V80 \_ BESTVBRVideo   | 品質受限之 VBR 內容的最佳品質型設定檔。                                                                                             |



 

系統設定檔可針對英文以外的語言進行當地語系化。 如需詳細資訊，請參閱 [當地語系化的系統設定檔](localized-system-profiles.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**IWMProfileManager2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




