---
description: Windows Management Instrumentation (wmi) 的主要工具之一，就是能夠查詢 wmi 存放庫中的類別和實例資訊。
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: 查詢 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc9cd51946bad1df482bb286c538e38bba8e2b3337776e3cd62e0a0da652574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817536"
---
# <a name="querying-wmi"></a>查詢 WMI

Windows Management Instrumentation (wmi) 的主要工具之一，就是能夠查詢 wmi 存放庫中的類別和實例資訊。 例如，您可以要求 WMI 傳回代表桌面系統關機事件的所有物件。 您也可以取出類別、實例或架構資料。 下表列出您可以進行的不同查詢類型。



| 主題                                                                | 描述                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [叫用同步查詢](invoking-a-synchronous-query.md)     | 描述如何在整個查詢過程中維護 WMI 的連結。 同步查詢適用于對本機系統進行小型查詢或查詢。<br/>                                  |
| [叫用非同步查詢](invoking-an-asynchronous-query.md) | 說明如何設定個別的進程來接收查詢。 非同步查詢比較複雜，並提供較低層級的安全性，但通常可改善系統效能。<br/> |



 

除了查詢 WMI 儲存機制，您也可以使用 [*WMI 查詢語言 (WQL)*](gloss-w.md) 將通知事件路由傳送至您的應用程式。 如需詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。

> [!Note]
>
> 若要適當地查詢 WMI，您必須對 WQL 有充分的瞭解。 不正確、太複雜或不當的查詢可能會導致查詢處理器傳回錯誤或非預期的結果。 如需 WQL 的完整指南，請參閱 [使用 Wql 查詢](querying-with-wql.md)。
>
> WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。 複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。 WQL 關鍵字的限制取決於查詢的複雜程度。
>
> 使用指令碼語言（例如 VBScript）查詢具有 **uint64** 或 **sint64** 資料類型的屬性值時，WMI 會傳回字串值。 比較這些值時，可能會發生非預期的結果，因為比較字串會傳回與比較數位不同的結果。 例如，比較字串時，"10000000000" 小於 "9"，而在比較數位時，則為9小於10000000000。 為了避免混淆，當從 WMI 抓取類型 **uint64** 或 **sint64** 的屬性時，您應該使用 VBScript 中的 [CDbl](/previous-versions//ftekwwt0(v=vs.85))方法。

 

> [!Note]  

 

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

 

