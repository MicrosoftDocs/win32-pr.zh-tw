---
description: 地區設定 \_ SPARENT
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11383e6fcdd216a1837d9f2f31e70a26821d394c3c56ea614b1df197bbe35c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105918"
---
# <a name="locale_sparent"></a>地區設定 \_ SPARENT

**Windows Vista 和更新版本：** 資源載入器所使用的備用地區設定。 此字串允許的最大字元數為85，包括結束的 null 字元。

地區設定具有特定地區設定的父系為中性地區設定的階層。 特定地區設定會與語言和國家/地區相關聯，而中性地區設定會與語言相關聯，但不會與任何國家/地區相關聯。 當特定地區設定的資源無法使用時，會使用父地區設定來決定要嘗試的第一個回復。 例如，"en-us" (0x0409) 的父地區設定為 "en" (0x0009) 。 當資源無法用於特定的 "en-us" 地區設定時，資源載入器會切換回使用可用於中性 "en" 地區設定的資源。 如需資源載入器回溯策略的進一步詳細資料，請參閱 [消費者介面語言管理](user-interface-language-management.md) 。

這個模式在預先定義的地區設定中是一致的。 不過，父地區設定並不是由地區設定名稱的任何操作所決定。 也就是說， [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 不會剖析字串（例如 "en-us"）以取得值 "en"。 相反地，他們會查看儲存的地區設定資料。 針對預先定義的地區設定，此值會遵循預期的模式，在此模式中，特定地區設定的父系是對應的中性地區設定，而中性地區設定的父系是不變的地區設定。 雖然建議自訂地區設定遵循類似的策略來定義其父地區設定，但這並不會強制執行。 執行自訂地區設定的應用程式可以指定較不明顯的適當父系。

> [!Note]  
> 由於 [呼叫「地區設定名稱](calling-the--locale-name--functions.md) 」函式中所述的任何函式都不接受中性地區設定做為輸入，因此此地區設定 \_ SPARENT 資料的用途有限。 尤其是， [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 都不接受中性地區設定做為輸入。

 

 

 



