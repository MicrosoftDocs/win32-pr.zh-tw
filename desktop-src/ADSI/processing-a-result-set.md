---
title: 處理結果集
description: 結果集會以一連串的資料列傳回。
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316450"
---
# <a name="processing-a-result-set"></a><span data-ttu-id="d2656-103">處理結果集</span><span class="sxs-lookup"><span data-stu-id="d2656-103">Processing a Result Set</span></span>

<span data-ttu-id="d2656-104">結果集會以一連串的資料列傳回。</span><span class="sxs-lookup"><span data-stu-id="d2656-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="d2656-105">每個資料列不一定會包含指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="d2656-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="d2656-106">使用 OLE DB 提供者時，結果集會像一般 SQL 結果集般出現。</span><span class="sxs-lookup"><span data-stu-id="d2656-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="d2656-107">如果您將 ADO 用於查詢， [ADODB。記錄集](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) 物件是用來遍歷結果集。</span><span class="sxs-lookup"><span data-stu-id="d2656-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="d2656-108">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (僅適用于支援 vtable 系結的語言，) 包含可在指定資料列中移動資料列資料指標和檢查屬性值的成員。</span><span class="sxs-lookup"><span data-stu-id="d2656-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="d2656-109">或者，您可以使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 來取得和設定屬性。</span><span class="sxs-lookup"><span data-stu-id="d2656-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 