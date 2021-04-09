---
description: 交易式 NTFS (TxF) 函數。
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: TxF 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694528"
---
# <a name="txf-functions"></a><span data-ttu-id="305db-103">TxF 函數</span><span class="sxs-lookup"><span data-stu-id="305db-103">TxF Functions</span></span>

<span data-ttu-id="305db-104">交易式 NTFS (TxF) 提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="305db-104">Transactional NTFS (TxF) provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="305db-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="305db-105">In this section</span></span>



| <span data-ttu-id="305db-106">函式</span><span class="sxs-lookup"><span data-stu-id="305db-106">Function</span></span>                                                                      | <span data-ttu-id="305db-107">描述</span><span class="sxs-lookup"><span data-stu-id="305db-107">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="305db-108">**TxfLogCreateFileReadCoNtext**</span><span class="sxs-lookup"><span data-stu-id="305db-108">**TxfLogCreateFileReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | <span data-ttu-id="305db-109">建立要用來讀取複寫記錄的內容。</span><span class="sxs-lookup"><span data-stu-id="305db-109">Creates a context to be used to read replication records.</span></span><br/>                                                         |
| [<span data-ttu-id="305db-110">**TxfLogDestroyReadCoNtext**</span><span class="sxs-lookup"><span data-stu-id="305db-110">**TxfLogDestroyReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | <span data-ttu-id="305db-111">關閉 [**TxfLogCreateFileReadCoNtext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) 函數所建立的讀取內容。</span><span class="sxs-lookup"><span data-stu-id="305db-111">Closes a read context created by the [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) function.</span></span><br/> |
| [<span data-ttu-id="305db-112">**TxfLogReadRecords**</span><span class="sxs-lookup"><span data-stu-id="305db-112">**TxfLogReadRecords**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | <span data-ttu-id="305db-113">從記錄檔讀取重做記錄。</span><span class="sxs-lookup"><span data-stu-id="305db-113">Reads the redo records from the log.</span></span><br/>                                                                              |



 

 

 




