---
title: 您可以知道什麼，以及何時可以知道
description: 區分延遲引發狀態的應用程式必須辨識問題狀態，並採取適當的動作。
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969432"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="e4048-103">您可以知道什麼，以及何時可以知道？</span><span class="sxs-lookup"><span data-stu-id="e4048-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="e4048-104">區分延遲引發狀態的應用程式必須辨識問題狀態，並採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="e4048-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="e4048-105">有兩個問題狀態：版本扭曲和部分更新。</span><span class="sxs-lookup"><span data-stu-id="e4048-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="e4048-106">藉由檢查目錄服務來偵測版本扭曲， (記得 [Active Directory Domain Services 使用此複寫模型](why-active-directory-domain-services-uses-this-replication-model.md)) 的原因所述的分散式運算條真理。</span><span class="sxs-lookup"><span data-stu-id="e4048-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="e4048-107">您可以藉由將中繼資料加入組成相關集合的物件，來偵測部分更新。</span><span class="sxs-lookup"><span data-stu-id="e4048-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="e4048-108">這類中繼資料的建議會出現在本檔的後續章節中。</span><span class="sxs-lookup"><span data-stu-id="e4048-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="e4048-109">有一些規避策略可讓應用程式減少版本扭曲和部分更新的可能性。</span><span class="sxs-lookup"><span data-stu-id="e4048-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="e4048-110">本檔的後續章節也會討論這些策略。</span><span class="sxs-lookup"><span data-stu-id="e4048-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




