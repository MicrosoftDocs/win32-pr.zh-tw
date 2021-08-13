---
description: 自訂動作的叫用方式與標準動作相同，無論是明確調用或在順序資料表執行期間。
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: 叫用自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba80afbd573ffb77fddb7723c433b7476055da2dc11deda39bb3cae4148b7f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629751"
---
# <a name="invoking-custom-actions"></a>叫用自訂動作

自訂動作的叫用方式與標準動作相同，無論是明確調用或在順序資料表執行期間。 呼叫動作的方法有兩種：

-   您可以使用 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函數直接呼叫指定的動作。
-   最上層動作會呼叫包含自訂動作的順序資料表。 如需有關排程順序資料表中自訂動作的詳細資訊，請參閱 [排序自訂動作](sequencing-custom-actions.md)。

當安裝程式從 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函式或順序資料表取得動作名稱時，它會先搜尋該名稱的標準動作。 如果找不到標準動作，則安裝程式會查詢 [CustomAction 資料表](customaction-table.md) ，以檢查指定的動作是否為自訂動作。 如果指定的動作不是自訂動作，則安裝程式會查詢對話方塊 [資料表](dialog-table.md) 中的對話方塊。

 

 



