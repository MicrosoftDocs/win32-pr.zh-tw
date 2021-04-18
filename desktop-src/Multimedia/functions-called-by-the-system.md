---
title: 系統呼叫的函式
description: 系統呼叫的函式
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- 多媒體音訊、正常運作
- 音訊、等式函數
- 音訊壓縮管理員 (的功能) 、函式
- " (音訊壓縮管理員) 、函式、功能"
- 進行的函數
- 回呼函式
- 音訊壓縮管理員 (的功能) 、回呼函式
- " (的音訊壓縮管理員) 、回呼函式"
- 攔截程式
- 驅動程式程式
- 音訊壓縮管理員 (的) 、攔截程式
- " (的音效壓縮管理員) 、攔截程式"
- 音訊壓縮管理員 (等量) ，驅動程式程式
- " (音訊壓縮管理員) 的驅動程式程式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968695"
---
# <a name="functions-called-by-the-system"></a>系統呼叫的函式

系統會呼叫三種不同類型的應用程式定義函數。 回呼函式是您應用程式中的函式，系統會呼叫此函式以回應應用程式所提出的要求。 攔截程式可協助應用程式處理對話方塊的自訂。 驅動程式是應用程式本身的編解碼器、轉換器或篩選器的實作為。

回呼函數具有下列名稱：

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

使用中的大部分列舉函數都會使用回呼函數。 例如，當您呼叫列舉函式時，會透過回呼函數重複呼叫應用程式來列舉專案。

某些函式無法從這些回呼函數中呼叫。 無法呼叫的函式會操控列舉函式所使用的內部的型式結構。 下列函式不應該從回呼函數中呼叫：

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

系統會呼叫下列函數來協助應用程式處理對話方塊的自訂：

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

下列函式會指定為可讓應用程式使用自訂編解碼器、轉換器或篩選準則的原型。 符合這個原型的函式可能會做為引數傳遞至 [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) 函數。

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 