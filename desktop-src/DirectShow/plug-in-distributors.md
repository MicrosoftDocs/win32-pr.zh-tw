---
description: 外掛程式散發者
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: 外掛程式散發者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7817e5e31b29444cc596b0be583be2198adc018
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000040"
---
# <a name="plug-in-distributors"></a>外掛程式散發者

外掛程式散發者 (Pid) 是擴充篩選圖形管理員功能的一種方式。 外掛程式散發者是篩選圖形管理員在執行時間匯總的 COM 物件。 應用程式會透過篩選圖形管理員取得 PID 的存取權。

當篩選圖形管理員針對不支援的介面進行查詢時，它會在登錄中搜尋下列格式的索引鍵：


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` 這是包含介面識別碼的字串。 如果登錄專案存在，專案的值會定義支援介面之 PID (CLSID) 的類別識別碼。 篩選圖形管理員會匯總 PID 並傳回介面指標，進而作為 PID 的外部 **IUnknown** 。 當應用程式呼叫介面上的方法時，實際上是在 PID 上呼叫它們。 不過，PID 的存在對應用程式而言是透明的。

「散發者」 *一詞是指 PID* 可以查詢其外部 **IUnknown** 指標，以取得篩選圖形管理員上的介面。 藉由呼叫 [**IFilterGraph：： EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) 方法，PID 可以列舉圖形中的篩選，並將方法呼叫散發至這些篩選器。 以這種方式，PID 可以作為應用程式在篩選準則上呼叫方法的單一控制點。

當篩選圖形管理員匯總 PID 時，它會查詢 [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) 介面的 pid。 如果 PID 支援這個介面，則篩選圖形管理員會使用它來通知 PID 有關圖形中的變更：

-   當篩選圖形在執行、暫停和停止狀態之間切換時，它會呼叫 [**IDistributorNotify：： run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run)、 [**IDistributorNotify：:P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)或 [**IDistributorNotify：： Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop)。
-   設定參考時鐘時，篩選圖形管理員會呼叫 [**IDistributorNotify：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource)。
-   當加入或移除篩選，或變更 pin 連接時，篩選圖形管理員會呼叫 [**IDistributorNotify：： NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange)。

若要執行自訂 PID，請建立支援匯總的 COM 物件。 它必須支援篩選圖形管理員還不支援的介面。 （選擇性）它可以支援 **IDistributorNotify** 介面。

如果 PID 從篩選圖形管理員取得任何介面指標，則應該立即釋出。 否則，它可能會建立迴圈參考計數，這可能會導致無法終結篩選圖形管理員。 在任何情況下都不需要在篩選圖形管理員上保存參考計數，因為篩選圖形管理員會控制 PID 的存留期。

因為 PID 是特別針對篩選圖形管理員所設計，所以您可能想要在 PID 的函式方法中強制執行此程式。 檢查外部 **IUnknown** 指標是否為 **Null**，如果是，則傳回錯誤碼 VFW \_ E \_ 需要擁有者 \_ 。  (查看 [錯誤和成功碼](error-and-success-codes.md)。也 ) 為了防止其他物件匯總 PID，您可以查詢 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)介面的外部 **IUnknown** 指標。 如果物件未公開 **IGraphBuilder**，則傳回錯誤碼。

 

 



