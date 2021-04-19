---
description: 衍生自 CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: 衍生自 CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970517"
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

 

 



