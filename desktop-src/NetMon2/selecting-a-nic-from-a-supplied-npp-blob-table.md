---
description: 若要從提供的 NPP BLOB 資料表中選取 (NIC) 的網路介面卡，請呼叫 SelectNPPBlobFromTable 函數。
ms.assetid: e75b6bb7-cf21-4e25-80a5-3b35f7ed0d0e
title: 從提供的 NPP BLOB 資料表選取 NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0215ca258c02745a7e5b4c285d6bf7df98a49e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986863"
---
# <a name="selecting-a-nic-from-a-supplied-npp-blob-table"></a><span data-ttu-id="c404e-103">從提供的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="c404e-103">Selecting a NIC from a Supplied NPP BLOB table</span></span>

<span data-ttu-id="c404e-104">若要從提供的 NPP BLOB 資料表中選取 (NIC) 的網路介面卡，請呼叫 [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="c404e-104">To select a network interface card (NIC) from a supplied NPP BLOB table, call the [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) function.</span></span> <span data-ttu-id="c404e-105">此函式會使用網路監視器 UI 來顯示 BLOB 資料表中所表示的 Nic，並傳回代表所選 NIC 的 NPP BLOB。</span><span class="sxs-lookup"><span data-stu-id="c404e-105">This function uses the Network Monitor UI to display the NICs represented in the BLOB table and returns the NPP BLOB that represents the selected NIC.</span></span>

<span data-ttu-id="c404e-106">當您呼叫 [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) 函數時，會出現 [ **選取網路** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c404e-106">When you call the [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="c404e-107">您可以在此查看 NPP BLOB 資料表中所代表 NPPs 的詳細資料、選取特定的 NIC，並查看其相關聯 NPP BLOB 結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c404e-107">From it, you can view the details of the NPPs represented in the NPP BLOB table, select a specific NIC, and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="c404e-108">下圖顯示提供的 NPP BLOB 資料表中所表示的 Nic。</span><span class="sxs-lookup"><span data-stu-id="c404e-108">The following illustration shows the NICs represented in a supplied NPP BLOB table.</span></span>

![在提供的 npp blob 資料表中表示的 nic](images/networkdb2.png)



| <span data-ttu-id="c404e-110">如需下列項目的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="c404e-110">For more information about</span></span>                        | <span data-ttu-id="c404e-111">請參閱</span><span class="sxs-lookup"><span data-stu-id="c404e-111">See</span></span>                                                                                                      |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c404e-112">選取在本機電腦上註冊的 NIC。</span><span class="sxs-lookup"><span data-stu-id="c404e-112">Selecting a NIC registered on the local computer.</span></span> | [<span data-ttu-id="c404e-113">如何選取已註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="c404e-113">How to select a registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="c404e-114">正在抓取 NPP BLOB 資料表。</span><span class="sxs-lookup"><span data-stu-id="c404e-114">Retrieving an NPP BLOB table.</span></span>                     | [<span data-ttu-id="c404e-115">如何從傳回的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="c404e-115">How to select a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



