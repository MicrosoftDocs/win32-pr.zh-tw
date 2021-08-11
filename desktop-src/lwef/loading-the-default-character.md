---
title: 正在載入預設字元
description: 正在載入預設字元
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f99d194843c6196f69e287857ce08097e849f328738c5f5d1a6e7feba0c53d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247605"
---
# <a name="loading-the-default-character"></a>正在載入預設字元

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

您可以載入 *預設字元*，而不是直接載入特定字元，而不是直接載入指定的字元。 預設字元是一種服務，其目的是要提供使用者選擇的共用、中央 Windows 助理。 Microsoft Agent 將屬性工作表包含為預設字元服務的一部分，也就是字元屬性視窗，可讓使用者變更選取的預設字元。

預設字元的選取範圍僅限於支援標準動畫集的字元，以確保跨字元的基本一致性層級。 這不會排除包含其他動畫的字元。

不過，因為預設字元是用於一般用途，而且可能會同時由其他應用程式共用，所以當您想要讓應用程式專用的字元時，請避免載入預設字元。

若要載入預設字元，請呼叫 [**load**](load-method.md) 方法，而不指定檔案名或路徑。 Microsoft Agent 會自動將目前的字元集載入為預設字元。 如果使用者尚未選取預設字元，則代理程式會選取支援標準動畫集的第一個字元。 如果沒有可用的，方法將會失敗，並回報原因。

雖然用戶端應用程式可以查詢字元的身分識別，但是只有使用者可以變更其設定。 您可以使用 [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) 來顯示屬性視窗字元。

當使用者變更選取的字元時，伺服器會通知已載入預設字元的用戶端，並傳遞新字元的 GUID。 伺服器會自動卸載先前的字元，並重載新的字元。 已載入預設字元之任何用戶端的佇列都會暫停和清除。 不過，使用字元的檔案名明確載入字元的用戶端佇列不會受到影響。 如有必要，伺服器也會處理新字元的文字轉換語音 (TTS) 引擎的自動重設。

 

 




