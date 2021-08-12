---
description: 網路應用程式有兩種基本類型：交易式和串流處理。 這些應用程式類型也分別稱為互動式和批次處理應用程式類型。
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: 交易式與串流應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e55a21ba552ed768b29b784a557633edfc5734ec266893ede04fded76e538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559494"
---
# <a name="transactional-versus-streaming-applications"></a>交易式與串流應用程式

網路應用程式有兩種基本類型： *交易* 式和 *串流處理*。 這些應用程式類型也分別稱為 *互動式* 和 *批次處理* 應用程式類型。

交易式應用程式是停止和移出應用程式。 它們通常會執行要求/回復作業，通常會進行排序。 交易式應用程式的範例包括同步遠端程序呼叫 (RPC) ，以及某些 HTTP 和網域名稱系統 (DNS) 的部署。

串流應用程式會移動資料。 若要使用平行詞彙來描述串流應用程式，串流應用程式會遵守流動性資料傳輸原理，通常只需考慮資料排序。 串流應用程式的範例包括網路備份和檔案傳輸協定 (FTP) 。

判斷應用程式類型之後，也會決定其網路和通訊協定特性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[效能維度](performance-dimensions-2.md)
</dt> </dl>

 

 



