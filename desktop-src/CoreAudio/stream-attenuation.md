---
description: 預設回避體驗
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: 預設回避體驗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec323bdaf01a7bba0821a9dee2c349239b3a53660334d2ac57edbf71287f396d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695011"
---
# <a name="default-ducking-experience"></a>預設回避體驗

假設使用者在接聽電腦上的音樂時收到通話。 在通話期間，使用者想要在接聽通話時減少音樂的音量等級，並在通話結束後繼續原始音量。 視使用者 **在 [音效** ] 控制台中指定的選項而定，作業系統會自動透過 *回避* 或 *串流衰減* 來提供此功能—減少音訊串流的強度。

預設衰減體驗取決於使用者的喜好設定，如 [控制台] 的 [ **音效** ] 選項中所指定。 在 [ **通訊** ] 索引標籤上，使用者可以選擇衰減層級 (預設值為 80% ) 、將所有非通訊串流靜音，或停用預設的串流衰減體驗。 系統允許新的非通訊資料流程 (但新的系統音效) 在通訊會話期間開啟，但不會自動衰減新的資料流程。 當所有的通訊資料流程都關閉時，系統會結束通訊會話，並還原在通訊會話期間衰減的資料流量。

為了以視覺化方式指出資料流程衰減，系統會根據使用者的喜好設定來變更磁片區混音器設定。 例如，如果使用者指定衰減層級，磁片區混音器會減少滑杆、顯示新的衰減磁片區，並顯示原始的音量層級。 下圖說明此程式。

![windows 7 中所提供之預設資料流程衰減行為的圖表](images/stream-aatenuation.jpg)

如果應用程式知道通訊會話的開始和結束時間，則應用程式可以覆寫資料流程衰減並執行自訂回避體驗。 如需詳細資訊，請參閱 [提供自訂回避行為](providing-a-custom-ducking-experience.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用通訊裝置](using-the-communication-device.md)
</dt> <dt>

[停用預設的回避體驗](disabling-the-ducking-experience.md)
</dt> <dt>

[提供自訂回避行為](providing-a-custom-ducking-experience.md)
</dt> <dt>

[回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[取得回避事件](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



