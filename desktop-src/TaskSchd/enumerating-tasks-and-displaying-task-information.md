---
title: 列舉工作和顯示工作資訊
description: 若要顯示工作的相關資訊，例如工作名稱、狀態或工作的最後一次執行，則可透過列舉工作資料夾中的執行中工作或工作，並顯示所需的資訊來完成。
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- 列舉工作工作排程器
- 工作排程器範例工作排程器，列舉工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4859122218ead4d18c1f9e83de0f55ce9373306cd2762e5608cf4d1841019b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002446"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>列舉工作和顯示工作資訊

若要顯示工作的相關資訊，例如工作名稱、狀態或工作的最後一次執行，則可透過列舉工作資料夾中的執行中工作或工作，並顯示所需的資訊來完成。

## <a name="accessing-properties-of-registered-tasks"></a>存取已註冊工作的屬性

若要顯示已註冊工作的屬性值，您必須連接到工作排程器服務，然後取得工作資料夾的實例，其中包含您想要取得相關資訊的工作。 然後，您可以在工作資料夾中取得所有已註冊工作的集合。 然後，您會列舉每個已註冊的工作，並取得並顯示每個工作的屬性值。

## <a name="accessing-properties-of-running-tasks"></a>存取執行中工作的屬性

若要顯示執行中工作的屬性值，您必須連接到工作排程器服務，然後取得所有執行中工作的集合 (包括或排除隱藏的工作) 。 然後，您會列舉每個執行中的工作，並取得並顯示每個工作的屬性值。

## <a name="example"></a>範例

下列範例會列舉工作並顯示工作的名稱和狀態：

-   [顯示工作名稱和狀態 (腳本) ](displaying-task-names-and-state--scripting-.md)
-   [顯示工作名稱和狀態 (c + +) ](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




