---
title: WinSNMP 資料庫
description: Microsoft WinSNMP 執行會在資料庫中維護系統管理資訊的存放區。
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462133"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="ace30-103">WinSNMP 資料庫</span><span class="sxs-lookup"><span data-stu-id="ace30-103">The WinSNMP Database</span></span>

<span data-ttu-id="ace30-104">Microsoft WinSNMP 執行會在資料庫中維護系統管理資訊的存放區。</span><span class="sxs-lookup"><span data-stu-id="ace30-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="ace30-105">資料庫包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="ace30-105">The database includes the following information:</span></span>

-   <span data-ttu-id="ace30-106">網路和版本屬性。</span><span class="sxs-lookup"><span data-stu-id="ace30-106">Network and version properties.</span></span>

    <span data-ttu-id="ace30-107">此執行會使用這些屬性來判斷要用來完成傳輸要求的網路傳輸通訊協定和 SNMP 版本架構。</span><span class="sxs-lookup"><span data-stu-id="ace30-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="ace30-108">如需詳細資訊，請參閱 [關於 SNMP 版本](about-snmp-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="ace30-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="ace30-109">實體和內容轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="ace30-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="ace30-110">此模式會使用此模式來解讀 SNMP 實體和內容的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ace30-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="ace30-111">如需詳細資訊，請參閱 [設定實體和內容轉譯模式](setting-the-entity-and-context-translation-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="ace30-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="ace30-112">重新傳輸原則設定。</span><span class="sxs-lookup"><span data-stu-id="ace30-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="ace30-113">此執行會使用此設定來判斷是否應該執行應用程式的重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="ace30-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="ace30-114">此實值會儲存每個目的地實體的超時值和重試計數。</span><span class="sxs-lookup"><span data-stu-id="ace30-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="ace30-115">如需詳細資訊，請參閱 [關於重新傳輸](about-retransmission.md) 和 [管理重新傳輸原則](managing-the-retransmission-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="ace30-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




