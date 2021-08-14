---
description: CRM 元件可以安裝在 COM + 伺服器應用程式或 COM + 程式庫應用程式中。
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: 設定 COM + CRM 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79f8c9716a9a4db2888231c886d3d1a4d929dd1a8dfb9f9f359ab03ec7670b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307447"
---
# <a name="configuring-com-crm-components"></a>設定 COM + CRM 元件

CRM 元件可以安裝在 COM + 伺服器應用程式或 COM + 程式庫應用程式中。 不過，它們一定要在 COM + 伺服器應用程式中執行。 如果它們是安裝在 COM + 程式庫應用程式中，就無法在用戶端進程中使用。

如果 CRM 元件是安裝在程式庫應用程式中，則可供多個伺服器應用程式使用。 如果安裝在特定的伺服器應用程式中，則只有該特定伺服器應用程式才能使用這些應用程式。

若要在伺服器應用程式中啟用 CRM 的使用，請使用下列步驟：

1.  在 [元件服務] 的 [伺服器應用程式屬性] 頁面底下，按一下 [ **Advanced** ] 索引標籤。

2.  針對該伺服器應用程式，選取 [ **啟用補償資源管理員** ] 選項。 如果未選取此選項，在此伺服器應用程式中嘗試使用 CRM 的嘗試將會失敗。

    > [!Note]  
    > 如果安裝在程式庫應用程式中，則不需要針對該程式庫應用程式選取 [ **啟用補償資源管理員** ] 選項，但是必須針對要執行 CRM 的伺服器應用程式選取這個選項。

     

建議您在相同的應用程式中安裝特定 CRM 的 CRM 工作者和 CRM 補償器元件。

CRM 元件的建議設定如下所示。



| 元件           | 設定                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM 背景工作**      | transaction = requiredsync = yesJIT = yesthreading model = (或執行緒模型 = 公寓)      |
| **CRM 補償器** | transaction = disabledsync = disabledJIT = nothreading model = (或執行緒模型 = 公寓)  |



 

> [!Note]  
> 使用 CRM 的元件必須在註冊時明確指定執行緒模型。 不支援預設的「主要執行緒單元」。 唯一支援的兩個執行緒模型為「單元」和「兩者」。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



