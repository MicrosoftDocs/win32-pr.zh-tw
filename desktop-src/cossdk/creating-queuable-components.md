---
description: 具有至少一個 queuable 介面的元件是 queuable 元件。
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: 建立 Queuable 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385931"
---
# <a name="creating-queuable-components"></a>建立 Queuable 元件

具有至少一個 queuable 介面的元件是 *queuable 元件*。 對於要由佇列叫用的元件，介面必須標示為 queuable，而且元件必須安裝在佇列應用程式中。 不過，queuable 元件可以是非佇列應用程式的元件。

Queuable 介面必須只包含 in 參數-沒有 out 參數和傳回值。 這些特性是藉由在元件安裝期間分析類型資訊來進行驗證。 如果未 queuable 介面，則無法啟用包含元件之應用程式的佇列。

若要將 COM + 介面指定為 queuable，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。

2.  開啟您想要進行 queuable 之 COM + 應用程式元件的 [ **介面** ] 資料夾。

3.  以滑鼠右鍵按一下您要標示為 queuable 的介面，然後按一下 [ **屬性**]。

4.  在 [屬性] 對話方塊中，選取 [ **佇列** ] 索引標籤。

5.  啟用標示為已 **排入佇列** 的核取方塊。

    > [!Note]  
    > 如果 [已 **排入佇列** ] 核取方塊呈現灰色，則介面不符合上述的 queuable 條件約束。

     

6.  按一下 [確定]  。

    Queuable 元件的識別方式是將 QUEUEABLE 屬性宏新增至介面定義語言的介面區段 (IDL) 原始程式檔，以取得 queuable 的所有介面。

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立元件佇列](creating-component-queues.md)
</dt> <dt>

[開發已排入佇列的元件](developing-queued-components.md)
</dt> </dl>

 

 



