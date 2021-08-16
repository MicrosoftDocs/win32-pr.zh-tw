---
description: 圖示重迭處理常式是以同進程元件物件模型 (COM) 物件，這些物件會實作為 Dll。
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: 如何實行圖示重迭處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8745d0d5c0cf9c69f28f0235ecc82acb07a14f1e3408d7fa7d65cf729e01403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859695"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>如何實行圖示重迭處理常式

圖示重迭處理常式是以同進程元件物件模型 (COM) 物件，這些物件會實作為 Dll。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier)之外，也會匯出一個介面。 這個介面有三個方法： [**IShellIconOverlayIdentifier：： GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo)、 [**IShellIconOverlayIdentifier：： GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)和 [**IShellIconOverlayIdentifier：： IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof)。

## <a name="instructions"></a>指示

### <a name="step-1-implementing-getoverlayinfo"></a>步驟1：執行 GetOverlayInfo

[**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo)方法會在初始化期間第一次呼叫。 方法會傳回包含圖示重迭影像之檔案的完整路徑，以及檔案內以零為基底的索引。 然後，Shell 會將影像加入至系統映射清單。 圖示重迭可以包含在任何標準檔案類型中，包括 .exe、.dll 和 .ico。

初始化完成之後，當 Shell 需要顯示處理常式的圖示重迭時，就會呼叫 [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) 。 方法應該會傳回在初始化期間所執行的相同檔案名和索引。 雖然 Shell 使用系統映射清單中快取的影像，而不是從檔案載入影像，但仍會以檔案名和索引來識別圖示重迭。

### <a name="step-2-implementing-getpriority"></a>步驟2：執行 GetPriority

[**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)方法只會在初始化期間呼叫。 它會將優先權值指派給處理常式的圖示重迭。 值的範圍可以從零到100，其中100是最低優先權。 這個優先權值的目的是要協助 Shell 解決針對單一物件指定多個圖示重迭時所發生的衝突。 Shell 會先使用一組內部規則來判斷最高優先順序的圖示重迭。 如果這些規則無法解決衝突，則依 **GetPriority** 指派給圖示重迭的值會決定優先順序。

[**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)所設定的優先順序值不是解決不相關之圖示重迭處理常式之間衝突的可靠方法。 您的處理常式無法判斷其他處理常式所使用的優先順序值。 一般來說，您應該將值設為零。 但是，當您已完成可要求相同物件之圖示重迭圖示的兩個或多個圖示重迭處理常式時，優先順序值會很有用。 藉由適當地設定優先順序值，您可以指定所要求的圖示重迭將顯示哪些。

### <a name="step-3-implementing-ismemberof"></a>步驟3：執行 IsMemberOf

Shell 會呼叫 [**IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) 方法，以判斷是否應該顯示特定物件的處理常式圖示重迭。 Shell 會將物件的名稱傳遞給方法，以指定物件。 如果處理常式想要顯示其圖示重迭， **IsMemberOf** 會傳回 S \_ OK。 如果沒有，則會傳回 \_ FALSE。

圖示重迭處理常式通常用於處理特定的檔案群組。 一般範例是以特定的副檔名來識別的 [檔案類型](fa-file-types.md)。 圖示重迭處理常式可以要求所有檔案類型檔案的圖示重迭。 某些處理常式只有在檔案類型的檔案處於特定狀態時，才會要求圖示重迭。 不過，圖示重迭處理常式可自由要求其所選物件的圖示重迭。

 

 
