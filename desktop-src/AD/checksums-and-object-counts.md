---
title: 總和檢查碼和物件計數
description: 總和檢查碼和物件計數是偵測策略，可讓應用程式偵測部分更新狀態。
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461964"
---
# <a name="checksums-and-object-counts"></a><span data-ttu-id="642a0-103">總和檢查碼和物件計數</span><span class="sxs-lookup"><span data-stu-id="642a0-103">Checksums and Object Counts</span></span>

<span data-ttu-id="642a0-104">總和檢查碼和物件計數是偵測策略，可讓應用程式偵測部分更新狀態。</span><span class="sxs-lookup"><span data-stu-id="642a0-104">Checksums and object counts are detection strategies that allow an application to detect a partial update state.</span></span> <span data-ttu-id="642a0-105">您也可以使用總和檢查碼來偵測衝突解決所引進的不一致。</span><span class="sxs-lookup"><span data-stu-id="642a0-105">Checksums can also be used to detect inconsistencies introduced by collision resolution.</span></span> <span data-ttu-id="642a0-106">總和檢查碼和物件計數都需要一個位置來儲存用來驗證總和檢查碼或物件計數的值。</span><span class="sxs-lookup"><span data-stu-id="642a0-106">Both checksums and object counts require a place to store the value used for verifying a checksum or object count.</span></span> <span data-ttu-id="642a0-107">這可以在與應用程式特定關聯性相關的「主要」物件上，或是在儲存相關物件的父物件上。</span><span class="sxs-lookup"><span data-stu-id="642a0-107">This can be on a "master" object chosen from among those involved in the application-specific relationship or on a parent object under which the related objects are stored.</span></span>

<span data-ttu-id="642a0-108">若為總和檢查碼，讀取相關物件的應用程式會藉由計算本機結果並與儲存的值進行比較，以驗證總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="642a0-108">For checksums, applications reading the related objects verify the checksum by calculating a local result and comparing it with the stored value.</span></span> <span data-ttu-id="642a0-109">如果值不相符，則複本會處於部分更新狀態，而且無法使用物件。</span><span class="sxs-lookup"><span data-stu-id="642a0-109">If the values do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="642a0-110">針對物件計數，應用程式會計算相關物件 (通常是單一父) 的子系，並將計數與儲存的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="642a0-110">For object counts, applications count the related objects (typically children of a single parent) and compare the count with the stored value.</span></span> <span data-ttu-id="642a0-111">如果計數不相符，則複本會處於部分更新狀態，而且無法使用物件。</span><span class="sxs-lookup"><span data-stu-id="642a0-111">If the counts do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="642a0-112">一些重要考量︰</span><span class="sxs-lookup"><span data-stu-id="642a0-112">Some important considerations:</span></span>

-   <span data-ttu-id="642a0-113">若要讓總和檢查碼方法能夠運作，必須更新用來計算總和檢查碼的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="642a0-113">For the checksum approach to work, the one or more attributes used in computing the checksum must be updated.</span></span> <span data-ttu-id="642a0-114">用來計算總和檢查碼的演算法必須可靠地反映輸入中的差異。</span><span class="sxs-lookup"><span data-stu-id="642a0-114">The algorithm used to compute the checksum must reliably reflect differences in input.</span></span> <span data-ttu-id="642a0-115">如果許多不同的輸入產品都有相同的總和檢查碼，演算法將無法可靠地偵測部分更新。</span><span class="sxs-lookup"><span data-stu-id="642a0-115">If many different inputs product the same checksum, the algorithm will not reliably detect partial updates.</span></span> <span data-ttu-id="642a0-116">「進行 salt 處理」輸入值（例如來源電腦的 **objectGUID** ）和更新的日期和時間也很有用。</span><span class="sxs-lookup"><span data-stu-id="642a0-116">"Salting" the input with values like the **objectGUID** of the source computer and the date and time of the update is also helpful.</span></span>
-   <span data-ttu-id="642a0-117">當物件計數與新的物件集搭配使用，或與一致性 Guid 搭配使用時，物件計數的效果最佳 (參閱下一節，以取得) 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="642a0-117">Object counts work best when used with new sets of objects, or in combination with consistency GUIDs (see the next section for more information).</span></span> <span data-ttu-id="642a0-118">執行更新的應用程式必須事先知道當更新完成時，容器中的物件數目，或在更新進行時使用其他將容器標示為不正確方式 (例如，將計數設定為零) 。</span><span class="sxs-lookup"><span data-stu-id="642a0-118">The application performing the update must either know, in advance, the number of objects that will be in the container when the update is completed or use some other means of marking the container invalid while the update proceeds (for example, setting the count to zero).</span></span> <span data-ttu-id="642a0-119">完成更新之後，來源應用程式會將容器標示為包含的物件計數。</span><span class="sxs-lookup"><span data-stu-id="642a0-119">After completing the update the source application marks the container with the count of objects contained.</span></span>

 

 




