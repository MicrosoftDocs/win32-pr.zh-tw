---
description: 在叢集環境中使用 COM + CRM
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: 在叢集環境中使用 COM + CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317872"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>在叢集環境中使用 COM + CRM

在開發要在叢集環境中運作的 COM + Crm 時，要考慮的主要因素是，特定 CRM 是否在意其正在操作的叢集節點。 例如，如果 CRM 所管理的資源是電腦檔案系統或登錄，則所有變更都是 CRM 伺服器應用程式在當時執行的節點所特有。 在此情況下，不需要將 CRM 伺服器應用程式容錯移轉至另一個節點。 在不同的情況下，CRM 會管理叢集的一些資源，而將 CRM 伺服器應用程式容錯移轉至另一個節點會很有用。

CRM 記錄檔的預設目錄位置與 DTC 記錄檔的目錄相同。 在叢集上，DTC 記錄檔會放在叢集節點之間容錯移轉的共用磁片上。 這表示 CRM 伺服器應用程式的預設行為是在叢集的節點之間進行容錯移轉。 因此，如果特定 CRM 需要不同的行為，而不是在節點之間進行容錯移轉，則應該變更該特定 CRM 伺服器應用程式之 CRM 記錄檔的位置。

此外，如果 CRM 應用程式需要容錯移轉，則應該將它設定為叢集群組中的一般應用程式。 其相依性應該是 DTC。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



