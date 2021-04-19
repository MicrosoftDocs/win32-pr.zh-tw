---
description: 當您選取已註冊的網路介面卡 (NIC) 列在本機電腦上時，可以使用篩選 BLOB 來忽略您不感興趣的 Nic。
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: 指定篩選 BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973491"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="f16c7-103">指定篩選 BLOB</span><span class="sxs-lookup"><span data-stu-id="f16c7-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="f16c7-104">當您選取已註冊的網路介面卡 (NIC) 列在本機電腦上時，可以使用 [*篩選 BLOB*](f.md) 來忽略您不感興趣的 nic。</span><span class="sxs-lookup"><span data-stu-id="f16c7-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="f16c7-105">例如，您可以限制搜尋特定類型的卡片 (例如 ETHERNET) 或特定 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="f16c7-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="f16c7-106">在搜尋 NIC 期間，篩選 BLOB 中的每個專案都必須符合代表 NIC 的 NPP BLOB 中的對等專案。</span><span class="sxs-lookup"><span data-stu-id="f16c7-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="f16c7-107">篩選 Blob 也可以是 [*特殊的 blob*](s.md)。</span><span class="sxs-lookup"><span data-stu-id="f16c7-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="f16c7-108">呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數時，篩選 BLOB 會限制 [ **選取網路** ] 對話方塊中顯示的 nic。</span><span class="sxs-lookup"><span data-stu-id="f16c7-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="f16c7-109">呼叫 [**GetNPPBlobTable**](getnppblobtable.md) 函數時，篩選 blob 會限制在 BLOB 資料表中傳回的 nic。</span><span class="sxs-lookup"><span data-stu-id="f16c7-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="f16c7-110">若要使用篩選準則，您必須建立篩選 BLOB、設定您想要篩選的屬性值 (包括) 的任何特殊 BLOB 專案，然後指定 BLOB 篩選器和 [**GetNPPBlobTable**](getnppblobtable.md) 或 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f16c7-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="f16c7-111">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="f16c7-111">For information on</span></span>                                 | <span data-ttu-id="f16c7-112">請參閱</span><span class="sxs-lookup"><span data-stu-id="f16c7-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16c7-113">如何選取在本機電腦上註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="f16c7-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="f16c7-114">選取已註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="f16c7-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="f16c7-115">正在抓取 NPP BLOB 資料表</span><span class="sxs-lookup"><span data-stu-id="f16c7-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="f16c7-116">從傳回的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="f16c7-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



