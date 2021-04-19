---
description: 您可以從兩個不同的觀點參考叢集：在檔案和磁片區中。
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: 叢集和延伸區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974475"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="63af4-103">叢集和延伸區</span><span class="sxs-lookup"><span data-stu-id="63af4-103">Clusters and Extents</span></span>

<span data-ttu-id="63af4-104">您可以從兩個不同的觀點參考叢集：在檔案和磁片區中。</span><span class="sxs-lookup"><span data-stu-id="63af4-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="63af4-105">檔案中的任何叢集都有 *虛擬叢集編號* (的 VCN) ，也就是從檔案開頭起算的相對位移。</span><span class="sxs-lookup"><span data-stu-id="63af4-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="63af4-106">例如，搜尋至叢集大小的兩倍，然後再讀取，將會傳回從第三個 VCN 開始的資料。</span><span class="sxs-lookup"><span data-stu-id="63af4-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="63af4-107">*邏輯叢集編號* (LCN) 描述叢集與磁片區中某個任意點的位移。</span><span class="sxs-lookup"><span data-stu-id="63af4-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="63af4-108">LCNs 只能視為序數或相對的數位。</span><span class="sxs-lookup"><span data-stu-id="63af4-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="63af4-109">邏輯群集不保證會對應到實體硬碟的磁區。</span><span class="sxs-lookup"><span data-stu-id="63af4-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="63af4-110">*範圍* 是連續叢集的執行。</span><span class="sxs-lookup"><span data-stu-id="63af4-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="63af4-111">例如，假設包含30個叢集的檔案記錄在兩個範圍內。</span><span class="sxs-lookup"><span data-stu-id="63af4-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="63af4-112">第一個範圍可能包含五個連續的叢集，另一個則是剩餘的25個群集。</span><span class="sxs-lookup"><span data-stu-id="63af4-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="63af4-113">在任何範圍的磁片上，並不保證任何其他範圍的任何關聯性。</span><span class="sxs-lookup"><span data-stu-id="63af4-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="63af4-114">例如，第一個範圍可能與後續的範圍在更高的 LCN。</span><span class="sxs-lookup"><span data-stu-id="63af4-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



