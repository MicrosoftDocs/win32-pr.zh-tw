---
description: 啟用元件佇列
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: 啟用元件佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385921"
---
# <a name="activating-component-queues"></a>啟用元件佇列

在已排入佇列的元件上進行方法呼叫，並不會直接執行方法。 相反地， [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 會將方法呼叫和參數封送處理並儲存在佇列中，而佇列中的這些呼叫和參數稍後會由佇列元件進行抓取和執行 與啟動遠端 DCOM 物件不同的是，在呼叫方法時，不會具現化已排入佇列的元件。 這是使用已排入佇列之元件背後的基本概念，佇列元件不需要與呼叫應用程式同時具現化。

> [!Note]  
> 啟用佇列應用程式的描述會假設應用程式已標示為已排入佇列，而且已啟用 [接聽程式] 核取方塊。

 

您可以使用腳本來啟動和停止已排入佇列的應用程式。 您可以將腳本放在工作排程器的控制項底下，以視需要執行。 例如，如果應用程式是可永久提供的，則腳本可以在系統重新開機時執行。 如果應用程式是以批次模式處理交易，則可以在每天的特定時間執行腳本，並搭配關機腳本，以確保批次處理會在特定時間停止。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要啟動已排入佇列的應用程式，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。

2.  以滑鼠右鍵按一下您想要啟用其佇列的應用程式。

3.  按一下 [啟動]。

## <a name="visual-basic"></a>Visual Basic

請參閱 COMAdminCatalog. StartApplication 範例。

## <a name="cc"></a>C/C++

請參閱 [**ICOMAdminCatalog：： StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用佇列的標記](using-the-queue-moniker.md)
</dt> </dl>

 

 



