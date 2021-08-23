---
description: 應用程式回收可以針對已知問題提供快速修正，以大幅提高 COM + 應用程式的整體穩定性，並協助防止非預期的問題。
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: COM + 應用程式回收概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a635487427fce3f17203f11426261996348a5e4057ab8bceebcae552d51bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129260"
---
# <a name="com-application-recycling-concepts"></a>COM + 應用程式回收概念

應用程式回收可以針對已知問題提供快速修正，以大幅提高 COM + 應用程式的整體穩定性，並協助防止非預期的問題。 例如，應用程式效能可能會因為問題（例如記憶體流失、nonscalable 資源使用量和進程失敗）而降級。 COM + 會提供應用程式回收，作為這些問題的解決方案。 您可以使用應用程式回收來自動關閉進程並重新啟動，進而重新初始化失敗的程式並重新配置其使用的記憶體。

應用程式回收的運作方式是建立與應用程式相關聯的 Dllhost.exe 進程複本。 這種重複的 Dllhost.exe 程式會提供未來所有物件要求的服務，讓舊的 Dllhost.exe 完成服務剩餘的物件要求。 當舊的 Dllhost.exe 進程偵測到進程中物件的所有外部參考，或達到到期超時值時，就會關閉。 透過此行為，應用程式回收可確保用戶端應用程式不會遇到服務中斷。

> [!Note]  
> 您無法回收已設定為以 Windows 服務的方式執行的 com + 應用程式。 此外，程式庫應用程式具有其主機進程的回收和共用屬性。

 

您可以使用 [元件服務] 系統管理工具，或透過 COM + 系統管理 SDK，以程式設計方式設定應用程式回收。 您可以根據 [**應用程式**](applications.md)集合中 [**COMAdminCatalogObject**](comadmincatalogobject.md)物件的下列屬性，以數個準則來回收進程：

-   **RecycleLifetimeLimit.** 進程回收之前可執行檔最大分鐘數。 有效範圍是從0到30240分鐘 (21 天) 。 預設分鐘數為0，表示進程不會回收達到存留期限制。
-   **RecycleMemoryLimit.** 在回收進程之前，進程記憶體使用量的最大數量 (以 kb) 。 如果進程記憶體使用量超過指定的數目超過一分鐘，則會回收進程。 有效範圍是0到 1048576 KB。 預設的記憶體使用量數量為 0 KB，表示進程將不會從達到記憶體限制時回收。
-   **RecycleCallLimit.** 應用程式物件在回收進程之前可以接受的呼叫數上限。 有效範圍是從0到1048576的呼叫。 預設的呼叫次數是0，表示進程不會從達到通話限制的情況下回收。
-   **RecycleActivationLimit.** 回收進程之前，要接受的應用程式物件啟用數目上限。 有效範圍是0到1048576的啟用。 預設啟用數目為0，表示處理常式將不會從達到啟用限制時回收。

此外，也會使用 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件的 RecycleExpirationTimeout 屬性來強制關閉回收進程。 它會指出在強制關閉進程之前，要等候回收進程中物件之所有外部參考的分鐘數。 有效範圍是從1到1440分鐘 (24 小時) ，而預設到期時間為15分鐘。 只有當已根據其他條件決定將回收處理程序時，才會使用此值。

您可以選取一個以上的準則來回收應用程式。 在滿足第一組準則之後，COM + 會回收應用程式。 您可以設定到期的到期時間值，以決定在強制關機之前，舊的 Dllhost.exe 進程可以花在完成剩餘服務要求的時間長度。

[**ApplicationInstances**](applicationinstances.md)集合提供 HasRecycled 屬性，此屬性可讓您判斷應用程式是否曾經被回收。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 應用程式回收工作](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



