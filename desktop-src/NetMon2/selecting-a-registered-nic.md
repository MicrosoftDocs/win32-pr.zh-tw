---
description: 若要選取在本機電腦上註冊的其中一個 Nic，請呼叫 GetNPPBlobFromUI 函數。
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: 選取已註冊的 NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974393"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="22d9c-103">選取已註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="22d9c-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="22d9c-104">若要選取在本機電腦上註冊的其中一個 Nic，請呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="22d9c-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="22d9c-105">此函式會使用網路監視器 UI 來顯示已註冊的 Nic，並傳回代表您所選 NIC 的 NPP BLOB。</span><span class="sxs-lookup"><span data-stu-id="22d9c-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="22d9c-106">您可以顯示在本機電腦或一組較小的已篩選 Nic 上註冊的所有 Nic。</span><span class="sxs-lookup"><span data-stu-id="22d9c-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="22d9c-107">若要篩選顯示的 Nic，請在進行呼叫時提供 [*篩選 BLOB*](f.md) 。</span><span class="sxs-lookup"><span data-stu-id="22d9c-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="22d9c-108">呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數時， [*NPP FINDER*](n.md) 會與 NPP dll 通訊，以取得代表已註冊 nic 的 NPP BLOB 結構。</span><span class="sxs-lookup"><span data-stu-id="22d9c-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="22d9c-109">如需詳細資訊，以及如何直接使用網路監視器 UI 的程式，請參閱網路監視器線上說明中的「選取網路對話方塊」主題。</span><span class="sxs-lookup"><span data-stu-id="22d9c-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="22d9c-110">當您呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數時，會出現 [ **選取網路** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="22d9c-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="22d9c-111">您可以在此查看在本機電腦上註冊的 NPPs 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="22d9c-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="22d9c-112">這項資訊包括本機 NPPs 和遠端 NPPs。</span><span class="sxs-lookup"><span data-stu-id="22d9c-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="22d9c-113">從對話方塊中，您可以選取特定的 NIC，並查看其相關聯 NPP BLOB 結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="22d9c-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="22d9c-114">下圖顯示網路監視器所提供之 NDIS NPP 的一般設定。</span><span class="sxs-lookup"><span data-stu-id="22d9c-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![網路監視器所提供之 ndis npp 的一般設定](images/networkdb.png)

<span data-ttu-id="22d9c-116">下表列出描述每個 NIC 選擇方法的主題。</span><span class="sxs-lookup"><span data-stu-id="22d9c-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="22d9c-117">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="22d9c-117">For information about</span></span>                                                                          | <span data-ttu-id="22d9c-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="22d9c-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d9c-119">如何指定篩選器來限制 [ **選取網路** ] 對話方塊中顯示的 nic。</span><span class="sxs-lookup"><span data-stu-id="22d9c-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="22d9c-120">指定篩選 BLOB</span><span class="sxs-lookup"><span data-stu-id="22d9c-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="22d9c-121">如何藉由呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數來選取 NIC。</span><span class="sxs-lookup"><span data-stu-id="22d9c-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="22d9c-122">使用 GetNPPBlobFromUI 選取 NIC</span><span class="sxs-lookup"><span data-stu-id="22d9c-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="22d9c-123">如何從提供的 NPP BLOB 資料表中選取 NIC。</span><span class="sxs-lookup"><span data-stu-id="22d9c-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="22d9c-124">從提供的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="22d9c-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



