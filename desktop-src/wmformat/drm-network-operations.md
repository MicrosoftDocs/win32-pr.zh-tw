---
title: DRM 網路作業
description: DRM 網路作業
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK，DRM 網路作業
- Advanced Systems Format (ASF) 、DRM 網路作業
- ASF (Advanced Systems Format) ，DRM 網路作業
- 數位版權管理 (DRM) ，網路作業
- DRM (數位版權管理) ，網路作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300224"
---
# <a name="drm-network-operations"></a><span data-ttu-id="03adc-108">DRM 網路作業</span><span class="sxs-lookup"><span data-stu-id="03adc-108">DRM Network Operations</span></span>

<span data-ttu-id="03adc-109">數個 DRM 相關的作業需要您的應用程式連接到在網路上執行的服務。</span><span class="sxs-lookup"><span data-stu-id="03adc-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="03adc-110">這些作業包括了個人化、授權取得、授權撤銷，以及授權備份和還原。</span><span class="sxs-lookup"><span data-stu-id="03adc-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="03adc-111">就像任何網路交易一樣，當您的應用程式包含需要網路作業的功能時，您的應用程式應該要考慮各種難題。</span><span class="sxs-lookup"><span data-stu-id="03adc-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="03adc-112">您的應用程式應該將作業的狀態追蹤至特定功能的任何可能範圍，通常是藉由處理狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="03adc-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="03adc-113">您應該將意見反應提供給使用者的狀態。</span><span class="sxs-lookup"><span data-stu-id="03adc-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="03adc-114">如果第一次嘗試時作業失敗，您應該讓使用者有機會重試。</span><span class="sxs-lookup"><span data-stu-id="03adc-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="03adc-115">在許多情況下，第一次嘗試會遇到困難，但後續的嘗試會完成，而不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="03adc-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="03adc-116">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="03adc-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="03adc-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="03adc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03adc-118">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="03adc-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




