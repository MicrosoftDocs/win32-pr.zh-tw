---
description: 儲存和還原 DvdState 物件
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: 儲存和還原 DvdState 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106995180"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>儲存和還原 DvdState 物件

[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) 物件可讓應用程式儲存使用者會話的快照集，包括光碟上的目前位置、正在觀賞之人員的家長監護、選取的音訊和子圖片串流等資訊。 這表示使用者可以將它們放在 DVD-Video 光碟上，並于稍後觀看。

應用程式無法建立 DvdState 物件。 當應用程式呼叫 [**IDvdInfo2：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate)時，DVD 導覽器會在內部建立這些物件。 DvdState 物件會公開 [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) 介面，以允許應用程式查詢特定資訊。

在 DVD 範例應用程式中， **CDvdCore：： RestoreBookmark** 和 **CDvdCore：： SaveBookmark** 函式會示範如何儲存和取出 DvdState 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



