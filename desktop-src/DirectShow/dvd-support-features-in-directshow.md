---
description: DirectShow 中的 DVD 支援功能
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: DirectShow 中的 DVD 支援功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f143bab35a8b9a4a0cb12af20c2c2c3b66a0822a24cfc054b1f5d30bd4bc3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107898"
---
# <a name="dvd-support-features-in-directshow"></a>DirectShow 中的 DVD 支援功能

[Dvd](dvd-navigator-filter.md)導覽篩選器的功能是透過兩個介面（ [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)）公開，這會提供 DVD 導覽器的「設定」方法，而 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)則提供「get」方法。

DVD 導覽器支援下列功能：

-   卡拉卡拉支援：您可以使用 DVD 導覽器來撰寫 DVD 卡拉卡拉應用程式。  (這需要相容的解碼器。 ) 
-   簡化 DVD 文字資訊字串的存取： DVD 導覽器會剖析這些字串，並讓應用程式輕鬆地列舉、識別及取出它們。
-   透過 IBasicAudio 的音訊音量控制[ ](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   支援在發出 Stop 命令時自訂 DVD 瀏覽器的行為：應用程式可以指示 DVD 導覽器在重新開機篩選圖形時，從目前的位置繼續，或從光碟開頭開始播放。
-   數位劇院系統 (DTS) 和索尼動態數位音效 (SDD) 音訊支援。 音訊瀏覽器會辨識 DTS 和 SDD 音訊串流，並傳遞給音訊解碼器。  (需要協力廠商 DTS 相容或 SDD 相容的解碼器，以解碼和播放音訊。 ) 
-   改進家長監護變更的支援： DVD 導覽器可讓應用程式接受、拒絕或忽略光碟中的家長監護變更命令。
-   管理 DVD 導覽器狀態和同步處理命令的 Advanced 選項
-   支援框架逐步執行、框架精確搜尋和反向播放。 這些功能需要支援的視頻解碼器。
-   將目前位置儲存在標題中的功能，並隨時返回。
-   針對非連續的 PGC 標題中的時間事件簡化支援：對於非連續的 PGC 標題，DVD 導覽器會將原始的時間代碼資訊轉送到應用程式。
-   時間碼資訊。 [**DVD \_ HMSF 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode)結構可用來取代二進位編碼的 decimal (BCD) 格式。 **DVD \_HMSF 時間 \_ 碼** 包含很容易存取的成員（小時、分鐘、秒和框架），而且可以在 **ULONG** 之間轉換。
-   控制篩選圖形是否在搜尋作業之後排清的能力：圖形緩衝區在任何指定時間最多可以包含幾秒鐘的影片。 您可以指示圖形在搜尋後完成播放已緩衝的影片，或立即在新位置開始播放。
-   在一般參數暫存器中設定值的能力，這是熟悉想要執行先進功能之 DVD 規格的先進功能。
-   產生數值光碟識別碼的能力，適用于所有實際用途

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>我需要什麼背景才能撰寫 DVD 應用程式？

所有應用程式開發人員都應該對 DVD 技術所提供的功能有基本的認識，例如家長管理層級、多個音訊和子圖片串流，以及角度區塊。 [DVD 基本概念](dvd-basics.md) 簡要說明這些功能;協力廠商發行集提供更完整的說明。 除非您想要在附錄 J 命令集以外執行先進的功能，否則不需要參照 DVD 規格。

使用 DirectShow 的 c/c + + 開發人員應該熟悉 com 用戶端程式設計技術，例如建立 com 物件以及取得和釋放 com 介面指標。 您可能也需要篩選圖形作業的一般知識，因為您可能需要直接存取和操作圖形。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



