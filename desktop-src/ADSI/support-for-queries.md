---
title: 支援查詢
description: 藉由執行 >idirectorysearch 介面，ADSI 提供者可以存取 OLE DB 唯讀功能的子集。
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- 支援查詢 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965556"
---
# <a name="support-for-queries"></a>支援查詢

藉由執行 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面，ADSI 提供者可以存取 OLE DB 唯讀功能的子集。

[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)本身的 adsi 實作為使用 Adsi 1.0 版中所述的 OLE DB 介面，包括下列 COM 物件清單：

-    (目錄服務的資料來源物件) ，支援 **IDBInitialize**、 **IDBCreateSession**、 **IDBProperties** 和 **IPersist**。
-   DBSessions 物件，支援 **IOpenRowSet**、 **ISessionProperties** 和 **ICreateCommand**。
-   Command 物件，支援 **ICommand**、 **IAccessor**、 **IColumnsInfo**、 **ICommandProperties**、 **ICommandText** 和 **IConvertType**。
-   Rowset 物件，支援 **IAccessor**、 **IColumnsInfo**、 **IConvertType**、 **IRowset** 和 **IRowsetInfo**。

如需 OLE DB 的詳細資訊，請參閱 OLE DB 程式設計人員在平臺軟體發展工具組中的參考 (SDK) 。

 

 




