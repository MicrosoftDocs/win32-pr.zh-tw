---
description: 識別有效的 DVD 作業
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: 識別有效的 DVD 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385779"
---
# <a name="identifying-valid-dvd-operations"></a>識別有效的 DVD 作業

有幾個因素會決定您是否可以執行指定的 DVD 操作：

-   目前的網域。 某些命令只有在某些網域中才有效。 當網域變更時，瀏覽器會傳送 EC \_ DVD \_ 網域 \_ 變更事件。 您也可以呼叫 [**IDvdInfo2：： GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) 來取得目前的網域。
-   UOPS 旗標。 這些是寫入光碟上的旗標，表示允許的作業。 每當旗標變更時，導覽器就會 \_ \_ \_ \_ 以新的旗標傳送 EC DVD 有效 UOPS 變更事件。 您也可以呼叫 [**IDvdInfo2：： GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) 來取得目前的 UOPS 旗標。
-   DVD 內容。 某些命令可能不會根據 DVD 的內容而相關。 例如，可能會根據目前的網域和 UOPS 旗標來允許 [**IDvdControl2：： SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) 方法，但影片可能只有一個角度。 在此情況下，允許 **SelectAngle** 呼叫但不是有意義的選項。

若有疑問，請允許動作。 在最糟的情況下， [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 方法將會失敗，而且您可以將意見反應提供給使用者。 意見反應應該相當不顯眼。 例如，您可能會快閃一個小的紅色 X 來警示使用者。 \_當網域禁止操作時，DVD 導覽器會傳回 VFW e \_ dvd \_ INVALIDDOMAIN，而 \_ \_ \_ \_ UOPS 旗標禁止操作時，會禁止 VFW E dvd 操作

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



