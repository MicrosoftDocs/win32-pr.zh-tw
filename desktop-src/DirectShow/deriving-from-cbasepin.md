---
description: 衍生自 CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: 衍生自 CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07eb76fc2913152a69ec729f49826e8b35f1524a3841c5e0d3085ea0634f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079258"
---
# <a name="deriving-from-cbasepin"></a>衍生自 CBasePin

若要使用 [**CBasePin**](cbasepin.md)來執行 pin，您必須從基類衍生新的類別，並覆寫數個方法。 您必須覆寫下列方法：

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

您可能需要覆寫這些額外的方法：

-   [**CBasePin：： Active**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin::EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin：：非使用中**](cbasepin-inactive.md)
-   [**CBasePin：： Notify**](cbasepin-notify.md)
-   [**CBasePin：： Run**](cbasepin-run.md)

最後，您必須執行 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 和 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

其中某些方法會在衍生自 **CBasePin** 的基類中執行，例如 [**CBaseInputPin**](cbaseinputpin.md) 和 [**CBaseOutputPin**](cbaseoutputpin.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



