---
description: 記錄是一種方式，可讓您在圖形中的節點或群組中的成員之間進行通訊。
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: 記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944758"
---
# <a name="records"></a><span data-ttu-id="6bade-103">記錄</span><span class="sxs-lookup"><span data-stu-id="6bade-103">Records</span></span>

<span data-ttu-id="6bade-104">記錄是一種方式，可讓您在圖形中的節點或群組中的成員之間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="6bade-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="6bade-105">記錄包含下列兩個部分：</span><span class="sxs-lookup"><span data-stu-id="6bade-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="6bade-106">記錄標頭</span><span class="sxs-lookup"><span data-stu-id="6bade-106">Record header</span></span>
-   <span data-ttu-id="6bade-107">特定的不透明資料內容</span><span class="sxs-lookup"><span data-stu-id="6bade-107">Specific opaque data content</span></span>

<span data-ttu-id="6bade-108">標頭包含記錄的相關資訊，包括發行的版本、建立者和資料類型。</span><span class="sxs-lookup"><span data-stu-id="6bade-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="6bade-109">標頭也包含 XML 屬性欄位，可讓應用程式加入描述資料的名稱/值屬性，並有效率地在記錄資料庫中搜尋先前發行的特定記錄。</span><span class="sxs-lookup"><span data-stu-id="6bade-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="6bade-110">內容是應用程式定義的資料，對等基礎結構而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="6bade-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="6bade-111">當記錄發佈時， (標頭和資料) 會在整個圖形或群組中溢滿。</span><span class="sxs-lookup"><span data-stu-id="6bade-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="6bade-112">同步對等會接收這項資料，並將它儲存在本機資料庫中。</span><span class="sxs-lookup"><span data-stu-id="6bade-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="6bade-113">未同步和離線的對等會在下一次連接時接收資料，並與對等圖形或群組進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="6bade-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="6bade-114">如需使用記錄的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="6bade-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="6bade-115">記錄相依性</span><span class="sxs-lookup"><span data-stu-id="6bade-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="6bade-116">記錄管理</span><span class="sxs-lookup"><span data-stu-id="6bade-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="6bade-117">記錄屬性架構</span><span class="sxs-lookup"><span data-stu-id="6bade-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="6bade-118">記錄搜尋查詢格式</span><span class="sxs-lookup"><span data-stu-id="6bade-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 



