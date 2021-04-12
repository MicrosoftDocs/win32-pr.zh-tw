---
description: 信封區段
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: 信封區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510070"
---
# <a name="envelope-segments"></a>信封區段

參數曲線是由一或多個使用 [**MP \_ 信封 \_ 區段**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) 結構所定義的信封區段所組成。 此結構包含下列資訊：

-   開始和結束時間。
-   開始和結束值。
-   曲線類型 (線性、正方形等) 。
-   選擇性旗標，稍後說明。

用戶端會藉由呼叫 [**IMediaParams：： AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) 方法並傳入 **MP \_ 信封 \_ 區段** 結構的陣列，將信封區段新增至參數。 在呼叫方法之前，用戶端應該將區段排序成遞增的時間順序。 當您處理資料時，可以想像出每個信封區段的參數移動，例如一系列 hills 的車輛駕駛。 [**IMediaParams：： GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam)方法會傳回最新的值。

兩個連續的區段之間可能會有間距。 在間距之間，參數會保留先前的值，如下所示：

-   在第一個區段之前，值是中性值。
-   在區段之間，值是上一個區段的結束值。
-   在最後一個區段之後，值會維持在該區段的結束值。
-   如果用戶端排清了，則值會還原為中性值。

您可以設定下列其中一個旗標來改變區段：

-   MPF \_ ENVLP \_ 開始 \_ CURRENTVAL。 SQL-DMO 使用參數的最新值做為區段的起始值。 這可能是中性值，或上一個區段的結束值。 SQL-DMO 會忽略 **MP \_ 信封 \_ 區段** 結構的 **valStart** 成員。
-   MPF \_ ENVLP \_ 開始 \_ NEUTRALVAL。 SQL-DMO 使用參數的中性值作為區段的起始值。 它會忽略 **valStart**。

您可以將這些旗標視為抓取區段的起點，並向上或向下移動，而結束值仍保持固定。 區段會據以「延展」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體參數](media-parameters.md)
</dt> </dl>

 

 



