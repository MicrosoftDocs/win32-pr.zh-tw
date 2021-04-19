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
# <a name="support-for-queries"></a><span data-ttu-id="22fad-104">支援查詢</span><span class="sxs-lookup"><span data-stu-id="22fad-104">Support for Queries</span></span>

<span data-ttu-id="22fad-105">藉由執行 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面，ADSI 提供者可以存取 OLE DB 唯讀功能的子集。</span><span class="sxs-lookup"><span data-stu-id="22fad-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="22fad-106">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)本身的 adsi 實作為使用 Adsi 1.0 版中所述的 OLE DB 介面，包括下列 COM 物件清單：</span><span class="sxs-lookup"><span data-stu-id="22fad-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="22fad-107"> (目錄服務的資料來源物件) ，支援 **IDBInitialize**、 **IDBCreateSession**、 **IDBProperties** 和 **IPersist**。</span><span class="sxs-lookup"><span data-stu-id="22fad-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="22fad-108">DBSessions 物件，支援 **IOpenRowSet**、 **ISessionProperties** 和 **ICreateCommand**。</span><span class="sxs-lookup"><span data-stu-id="22fad-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="22fad-109">Command 物件，支援 **ICommand**、 **IAccessor**、 **IColumnsInfo**、 **ICommandProperties**、 **ICommandText** 和 **IConvertType**。</span><span class="sxs-lookup"><span data-stu-id="22fad-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="22fad-110">Rowset 物件，支援 **IAccessor**、 **IColumnsInfo**、 **IConvertType**、 **IRowset** 和 **IRowsetInfo**。</span><span class="sxs-lookup"><span data-stu-id="22fad-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="22fad-111">如需 OLE DB 的詳細資訊，請參閱 OLE DB 程式設計人員在平臺軟體發展工具組中的參考 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="22fad-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




