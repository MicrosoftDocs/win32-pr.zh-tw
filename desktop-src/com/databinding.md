---
title: 資料繫結
description: 資料繫結
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2040aa29c83615f42c321483c87be378737dcdef47e43873fbe3b8c0902dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048366"
---
# <a name="databinding"></a>資料繫結

已加入新的資料系結屬性，只有當焦點離開控制項或在所有屬性變更通知期間，才會讓屬性區分通訊的變更。

新的屬性（稱為 ImmediateBind）可讓控制項區分兩種不同類型的可系結屬性。 其中一種可系結屬性必須通知資料庫的每項變更，例如，有一個核取方塊控制項，也就是每個變更都需要傳送到基礎資料庫，即使控制項尚未遺失焦點也一樣。 不過，例如 listbox 的控制項只會希望在控制項失去焦點時，將屬性的變更通知給資料庫，因為使用者可能會在尋找所要的設定之後，使用方向鍵來變更反白顯示的選取專案，讓變更通知在每次使用者按下方向鍵時，將變更通知傳送至資料庫，以提供無法接受的效能。 新的 [立即系結] 屬性可讓表單上的個別可系結屬性指定此行為，當設定此位時，將會通知所有變更。

新的 ImmediateBind 位會對應至新的 VARFLAG \_ FIMMEDIATEBIND (0x80) 和 FUNCFLAG \_ FIMMEDIATEBIND (0x80) 位在 VARFLAGS 介面的 FUNCFLAGS 和 ITypeInfo 列舉中[](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) ，以便檢查屬性屬性。

 

 