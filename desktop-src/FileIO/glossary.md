---
description: 用來描述交易式 NTFS (TxF) 的術語。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: TxF 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194756"
---
# <a name="txf-glossary"></a><span data-ttu-id="c6cc5-103">TxF 詞彙</span><span class="sxs-lookup"><span data-stu-id="c6cc5-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="c6cc5-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**可用 性**</span><span class="sxs-lookup"><span data-stu-id="c6cc5-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="c6cc5-105">可用性意指資源管理員會中止交易，即使這會中斷一致性，讓系統可以繼續執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="c6cc5-106">預設資源管理員會在系統磁碟區上強制執行可用性。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="c6cc5-107">例如，如果交易記錄檔已滿，就無法加入新的交易記錄空間，而將中止的較舊交易必須從高階資源管理員傳遞結果，才能讓分散式交易完成，資源管理員將不會等待較佳的交易管理員，也會中止交易，即使這可能會中斷一致性。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="c6cc5-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**一致性**</span><span class="sxs-lookup"><span data-stu-id="c6cc5-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="c6cc5-109">一致性表示如果新交易無法進行前進進度，則資源管理員將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="c6cc5-110">例如，如果交易記錄檔已滿，就無法加入新的交易記錄空間，而將中止的較舊交易必須從高階資源管理員傳遞結果，才能讓分散式交易完成，資源管理員會等待該結果。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="c6cc5-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**迷你**</span><span class="sxs-lookup"><span data-stu-id="c6cc5-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="c6cc5-112">迷你版本是交易寫入器在交易期間所建立的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="c6cc5-113">您稍後可以在具有唯讀存取權的交易中開啟迷你。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="c6cc5-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**交易讀取器**</span><span class="sxs-lookup"><span data-stu-id="c6cc5-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="c6cc5-115">交易式讀取器是以任何許可權開啟的交易式檔案控制代碼，該許可權屬於泛型讀取權限的一部分，但不屬於一般寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="c6cc5-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**交易寫入器**</span><span class="sxs-lookup"><span data-stu-id="c6cc5-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="c6cc5-117">交易寫入器是一種使用不屬於泛型讀取權限的任何許可權開啟的交易式檔案控制代碼，但屬於一般寫入存取權的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6cc5-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 



