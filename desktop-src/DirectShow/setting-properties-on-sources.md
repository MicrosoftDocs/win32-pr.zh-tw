---
description: 設定來源的屬性
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: 設定來源的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06908f4f15a6d1107ce15e71679c92ec8065725ed883a6561df5cd21af3e13c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965018"
---
# <a name="setting-properties-on-sources"></a>設定來源的屬性

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

當您建立新的來源物件時，有幾個您需要設定的屬性，以及您可以選擇性地設定的其他屬性。 您必須設定下列屬性。

-   相對於時間軸其餘部分的開始和停止時間。 呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 方法。 請勿在相同的播放軌內的來源物件上設定重迭的時間，否則會造成未定義的行為。
-   要做為來源剪輯使用的媒體檔案。 呼叫 [**IAMTimelineSrc：： SetMediaName**](iamtimelinesrc-setmedianame.md)。
-   相對於原始來源檔案的媒體開始和停止時間。 呼叫 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md) 方法。 例外狀況：如果來源是靜止影像，請勿指定媒體時間。 如需媒體時間的詳細資訊，請參閱[DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。

來源物件會從父群組繼承其媒體類型，因此不需要指定媒體類型。

選擇性屬性包含下列各項：

-   延展模式。 stretch 模式會指定 Microsoft® DirectShow®編輯服務 (DES) 如何轉譯其大小不符合輸出維度的來源。 根據預設，DES 會伸展影像，而不會保留長寬比。 或者，DES 可以裁剪映射或建立黑邊。 呼叫 [**IAMTimelineSrc：： SetStretchMode**](iamtimelinesrc-setstretchmode.md) 方法來指定延展模式。
-   來源檔案的持續時間。 如果您在設定媒體時間之前設定了此屬性，DES 會驗證媒體停止時間，並在超過檔案持續時間時截斷停止時間。 這有助於避免稍後轉譯錯誤。 您可以使用媒體偵測器來取得檔案的持續時間，如 [使用媒體](using-the-media-detector.md)偵測器中所述。 呼叫 [**IAMTimelineSrc：： SetMediaLength**](iamtimelinesrc-setmedialength.md) 方法來指定檔案持續時間。
-   資料流程號碼。 根據預設，來源物件會使用檔案中的第一個資料流程，該資料流程符合父群組的媒體類型。 如果檔案包含兩個或多個相同媒體類型的資料流程，請呼叫 [**IAMTimelineSrc：： SetStreamNumber**](iamtimelinesrc-setstreamnumber.md)來選取要使用的資料流程。 您可以使用媒體偵測器來尋找資料流程數目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用來源](working-with-sources.md)
</dt> </dl>

 

 



