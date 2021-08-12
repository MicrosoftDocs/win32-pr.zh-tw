---
title: 效能指導方針
description: 開發在遠端桌面服務環境中順利執行之應用程式的指導方針。
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a8211f12e4a89c5dfb309bb4e3c0f998159738b46185aeb5dcee7a5cd29f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605310"
---
# <a name="performance-guidelines"></a>效能指導方針

下列各節提供在遠端桌面服務環境中開發順利執行應用程式的指導方針。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[圖形效果](graphic-effects.md)
</dt> <dd>

在遠端桌面服務環境中做為遠端會話執行時，應該停用的功能清單。

</dd> <dt>

[遠端桌面服務中背景工作的指導方針](background-tasks.md)
</dt> <dd>

若要讓所有使用者都能發揮最大的 CPU 可用性，請在遠端桌面服務環境中執行時停用背景工作，或建立不需耗用大量資源的有效率背景工作。

</dd> <dt>

[執行緒使用方式](thread-usage.md)
</dt> <dd>

您應該針對多使用者、多處理器遠端桌面服務環境，調整應用程式執行緒的使用方式並進行平衡。

</dd> <dt>

[偵測遠端桌面服務環境](detecting-the-terminal-services-environment.md)
</dt> <dd>

為了將效能優化，應用程式可以偵測它們是否在遠端桌面服務用戶端會話中執行，是很好的作法。

</dd> </dl>

檢查您的應用程式是否發生記憶體流失問題，並解決任何問題。 當然，對於任何應用程式來說，這是很好的建議，但是在遠端桌面服務環境中，多個使用者可以多次執行應用程式，因此可快速放大記憶體流失的影響。

動畫、大型影像、音訊和其他頻寬密集型服務都必須可設定。 當這些服務不是主要功能時，它們預設可以針對遠端會話關閉，但在會話執行于本機或透過高頻寬連接時啟用。 如果應用程式的目的是要提供高頻寬的服務，例如串流影片廣播，則服務預設不需要關閉。

 

 




