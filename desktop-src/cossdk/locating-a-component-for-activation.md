---
description: 找出要啟用的元件
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: 找出要啟用的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104571572"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="72492-103">找出要啟用的元件</span><span class="sxs-lookup"><span data-stu-id="72492-103">Locating a Component for Activation</span></span>

<span data-ttu-id="72492-104">當 COM + 找到正確的資料分割時（透過使用者識別的預設資料分割集、資料分割的名字，或物件內容中的資料分割識別碼），COM + 必須在該資料分割內找出正確的元件。</span><span class="sxs-lookup"><span data-stu-id="72492-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="72492-105">下圖顯示元件位於分割區時，如何找到和啟動元件。</span><span class="sxs-lookup"><span data-stu-id="72492-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="72492-106">在啟動任何元件之前，COM + 會執行驗證，以確認嘗試啟用元件的使用者身分識別是否有許可權可以存取元件所在的分割集。</span><span class="sxs-lookup"><span data-stu-id="72492-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![此圖顯示用於尋找要啟用之元件的疑難排解樹狀目錄。](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="72492-108">上圖顯示下列內容：</span><span class="sxs-lookup"><span data-stu-id="72492-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="72492-109">如果所呼叫的元件位於分割區中，而且與呼叫元件位於相同的應用程式中，則不論所呼叫的元件是否標記為公用或私用，元件都會啟用。</span><span class="sxs-lookup"><span data-stu-id="72492-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="72492-110">如果所呼叫的元件位於分割區中，但不存在於與呼叫元件相同的應用程式中，COM + 會檢查元件是否標記為公用。</span><span class="sxs-lookup"><span data-stu-id="72492-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="72492-111">如果找不到任何公用版本，COM + 會搜尋全域分割區，以找出元件的公用版本。</span><span class="sxs-lookup"><span data-stu-id="72492-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="72492-112">如果在全域分割區中找不到元件的公用版本，或如果使用者身分識別沒有分割區的許可權，則啟用會失敗。</span><span class="sxs-lookup"><span data-stu-id="72492-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72492-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="72492-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72492-114">在啟用期間尋找磁碟分割</span><span class="sxs-lookup"><span data-stu-id="72492-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 



