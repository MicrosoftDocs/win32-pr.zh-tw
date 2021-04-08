---
title: 偵測和避免複寫延遲
description: 複寫延遲是在鬆散結合的分散式系統中的生活事實。
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671347"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="14362-103">偵測和避免複寫延遲</span><span class="sxs-lookup"><span data-stu-id="14362-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="14362-104">複寫延遲是在鬆散結合的分散式系統中的生活事實。</span><span class="sxs-lookup"><span data-stu-id="14362-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="14362-105">應用程式必須配合此。</span><span class="sxs-lookup"><span data-stu-id="14362-105">Applications must accommodate this.</span></span> <span data-ttu-id="14362-106">解決複寫延遲的最佳方式，是設計應用程式以將效果降到最低。</span><span class="sxs-lookup"><span data-stu-id="14362-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="14362-107">理想的啟用目錄應用程式：</span><span class="sxs-lookup"><span data-stu-id="14362-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="14362-108">不區分版本扭曲。</span><span class="sxs-lookup"><span data-stu-id="14362-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="14362-109">不相依于多個物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="14362-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="14362-110">沒有內部或物件間的一致性需求。</span><span class="sxs-lookup"><span data-stu-id="14362-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="14362-111">符合此設定檔的應用程式和服務不需要考慮複寫延遲。</span><span class="sxs-lookup"><span data-stu-id="14362-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="14362-112">其他應用程式必須以複寫延遲為考慮而設計。</span><span class="sxs-lookup"><span data-stu-id="14362-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="14362-113">設計這類應用程式成功的關鍵在於複寫程式的認知。</span><span class="sxs-lookup"><span data-stu-id="14362-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="14362-114">在設計階段用來減少物件間相依性，並將部分更新視窗降至最低的步驟，會在執行時間支付龐大的紅利。</span><span class="sxs-lookup"><span data-stu-id="14362-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="14362-115">處理複寫延遲的方法分為兩個類別，也就是避免延遲和偵測策略影響的策略，可讓應用程式偵測延遲引發的狀態。</span><span class="sxs-lookup"><span data-stu-id="14362-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




