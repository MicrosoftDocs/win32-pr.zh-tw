---
description: 包含至少一個 queuable 元件的應用程式，可以使用 [元件服務] 系統管理工具標示為已排入佇列。
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: 建立元件佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972556"
---
# <a name="creating-component-queues"></a>建立元件佇列

包含至少一個 queuable 元件的應用程式，可以使用 [元件服務] 系統管理工具標示為已排入佇列。

當應用程式標示為已排入佇列時，COM + 會自動為其建立訊息佇列的佇列。 佇列名稱是應用程式的名稱;如果佇列名稱與現有佇列的名稱相符，COM + 將會使用現有的佇列。

> [!Note]  
> 訊息佇列 *路徑* 名稱參數是遠端伺服器名稱 (RSN) 和 com + 應用程式名稱的組合。 RSN 指的是遠端啟用的目標。 您可以在用戶端電腦上安裝用戶端可匯出的應用程式期間指定 RSN。 此安裝程式會使用 RSN，將啟用直接導向至指定的用戶端電腦。 如需有關佇列名稱的詳細資訊，請參閱 [使用佇列](using-the-queue-moniker.md)的「佇列標記參數」一節中的參數表格。

 

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要將 COM + 應用程式指定為已排入佇列，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。

2.  以滑鼠右鍵按一下您要建立佇列的應用程式，然後按一下 [ **屬性**]。

3.  在 [屬性] 對話方塊中，選取 [ **佇列** ] 索引標籤。

4.  啟用標示為 [已 **排入佇列] 的核取方塊–此應用程式可由 MSMQ 佇列達成**。

    > [!Note]  
    > 如果 [已 **排入佇列** ] 核取方塊呈現灰色，則應用程式不會包含任何 queuable 元件。

     

5.  按一下 [確定]  。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

不適用。

## <a name="remarks"></a>備註

COM + 系統管理程式庫或 [元件服務] 系統管理工具所建立的佇列，會以訊息佇列的交易屬性標記。

在伺服器上安裝佇列應用程式之後，用戶端可以藉由匯出應用程式，然後在每個用戶端匯入應用程式，讓用戶端可以使用該應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 Queuable 元件](creating-queuable-components.md)
</dt> <dt>

[已排入佇列的元件架構](queued-components-architecture.md)
</dt> </dl>

 

 



