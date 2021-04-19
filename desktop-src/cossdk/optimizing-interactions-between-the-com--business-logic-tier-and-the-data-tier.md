---
description: 資料層通常會包含靜態資訊&\# 郵件; 保存在永久性媒體上的資訊。
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: 優化 COM + 商務邏輯與資料之間的呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972554"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="0fbcd-103">優化 COM + 商務邏輯層與資料層之間的互動</span><span class="sxs-lookup"><span data-stu-id="0fbcd-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="0fbcd-104">資料層通常會包含靜態資訊，也就是保存在永久性媒體上的資訊。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="0fbcd-105">因為這一層包含大部分是靜態的資訊，所以需要徹底分析潛在的瓶頸。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="0fbcd-106">除了明顯的連接瓶頸可能性，作用點可能是經常存取的記錄、無效率的資料存取方法，以及協調存取舊版系統的需求所造成。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="0fbcd-107">連接到資料層</span><span class="sxs-lookup"><span data-stu-id="0fbcd-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="0fbcd-108">在設計 COM + 應用程式的資料層時，有兩個考慮扮演重要角色：連接共用和 [Com + 及時 (JIT) 啟用](com--just-in-time-activation.md)，以及使用 dsn。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="0fbcd-109">建立資料層連接的元件應該使用元件上設定的 [Com + 物件](com--object-pooling.md) 共用。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="0fbcd-110">建立 Dsn 時，請使用在元件上指定的物件指定函式字串，而不是建立 File DSN。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="0fbcd-111">檔案 Dsn 比使用物件的函式字串的連接慢。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="0fbcd-112">可以在元件屬性工作表上指定物件的函式字串。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="0fbcd-113">如需詳細資訊，請參閱 [Com + 物件](com--object-constructor-strings.md)的函式字串。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="0fbcd-114">如果您使用元件來存取 SQL Server 資料庫，請使用 COM + 物件共用，而不是 SQL 連接共用。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="0fbcd-115">如果您的元件使用 ADO 提取多個記錄集，請建立元件的多個連接。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="0fbcd-116">當 ADO 抓取多個記錄集時，如果您未建立，就會在背景中建立多個連接。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="0fbcd-117">如果您建立它們，您可以將它們集區化，並對所使用的連線數目有更大的控制權。</span><span class="sxs-lookup"><span data-stu-id="0fbcd-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fbcd-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="0fbcd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fbcd-119">將 COM + 商務邏輯層和展示層之間的互動優化</span><span class="sxs-lookup"><span data-stu-id="0fbcd-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



