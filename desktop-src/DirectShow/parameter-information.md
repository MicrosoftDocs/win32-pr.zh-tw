---
description: 參數資訊
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: 參數資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe38cc9197df3ae22bcd72b824da5887647bca9e9d6101e3833d482fa907052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050768"
---
# <a name="parameter-information"></a>參數資訊

[**IMediaParamInfo：： GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo)方法會傳回用來描述參數的 [**MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo)結構。 此結構包含下列資訊：

-   **MpType** 成員會指出參數值的資料類型。 為了提高效率，所有參數都會實作為32位浮點值。 [**MP \_ 型**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type)別列舉會定義要將值轉譯為整數、浮點數、布林值或列舉 (整數系列) 。
-   **MopCaps** 成員會指出此參數支援的曲線。 如果資料類型是布林值或列舉，則參數可以支援的唯一曲線是「跳過」。
-   **MpdMinValue** 和 **mpdMaxValue** 成員會定義此參數的最小值和最大值。 此參數的任何曲線都必須落在此範圍內。
-   **MpdNeutralValue** 成員是參數的預設值。
-   **SzLabel** 成員是參數的名稱，而 **szUnitText** 成員是參數的測量單位的名稱。 範例可能包括「磁片區」、「分貝」或「頻率」和「kHz」。 這兩個字串都是英文，而且絕對不會當地語系化。 DMO 可以透過 [**IMediaParamInfo：： GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext)方法提供當地語系化版本。

在 DMO 的整個存留期間，每個參數的資訊都會保持固定。 因此，用戶端可以查詢此資訊一次，然後加以快取。

**時間格式**

用戶端必須時間戳記輸入資料，讓 DMO 可以計算對應的參數值。 根據預設，時間戳記代表單位為100毫微秒，也稱為 *參考時間*。 不過，此時間單位對每個應用程式來說都不方便，因此 DMO 有支援其他時間格式的選項。 時間格式是由 GUID 所識別。



| **GUID**              | 描述                   |
|-----------------------|-------------------------------|
| GUID \_ 時間 \_ 參考 | 參考時間                |
| GUID \_ 時間 \_ 音樂     | 每季的各部分附注 (PPQN)  |
| GUID \_ 時間 \_ 範例   | 每秒樣本數            |



 

建議協力廠商視需要定義自己的時間格式。 不過，所有 DMOs 都必須支援參考時間。 這會提供每個人都可以使用的標準基準。 若要判斷 DMO 支援多少時間格式，請呼叫 [**IMediaParamInfo：： GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats)方法。 若要列舉支援的格式，請呼叫 [**IMediaParamInfo：： GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) 方法。

若要設定時間格式，請呼叫 [**IMediaParams：： SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat)。 這個方法會指定時間格式的 GUID 和 *時間資料*，也就是每個時鐘的單位數刻度。 例如，如果時間格式為每秒的樣本，而時間資料為32，則時間戳記值10會對應到320範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體參數](media-parameters.md)
</dt> </dl>

 

 



