---
description: 音量信封效果
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: 音量信封效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983757"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="e1a17-103">音量信封效果</span><span class="sxs-lookup"><span data-stu-id="e1a17-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="e1a17-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e1a17-104">\[Deprecated.</span></span> <span data-ttu-id="e1a17-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e1a17-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1a17-106">音量信封效果會在音訊串流上設定音量。</span><span class="sxs-lookup"><span data-stu-id="e1a17-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="e1a17-107">類別識別碼 (CLSID) ： {036A9790-C153-11D2-9EF7-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="e1a17-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="e1a17-108">CLSID 變數名稱： CLSID \_ AudMixer</span><span class="sxs-lookup"><span data-stu-id="e1a17-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="e1a17-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e1a17-109">Properties</span></span>



| <span data-ttu-id="e1a17-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e1a17-110">Property</span></span> | <span data-ttu-id="e1a17-111">類型</span><span class="sxs-lookup"><span data-stu-id="e1a17-111">Type</span></span>   | <span data-ttu-id="e1a17-112">預設</span><span class="sxs-lookup"><span data-stu-id="e1a17-112">Default</span></span> | <span data-ttu-id="e1a17-113">描述</span><span class="sxs-lookup"><span data-stu-id="e1a17-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1a17-114">Vol</span><span class="sxs-lookup"><span data-stu-id="e1a17-114">Vol</span></span>      | <span data-ttu-id="e1a17-115">double</span><span class="sxs-lookup"><span data-stu-id="e1a17-115">double</span></span> | <span data-ttu-id="e1a17-116">1.0</span><span class="sxs-lookup"><span data-stu-id="e1a17-116">1.0</span></span>     | <span data-ttu-id="e1a17-117">磁片區，以撰寫之磁片區的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="e1a17-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="e1a17-118">您可以在一段時間內改變這個屬性值，以產生音訊淡化。</span><span class="sxs-lookup"><span data-stu-id="e1a17-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1a17-119">備註</span><span class="sxs-lookup"><span data-stu-id="e1a17-119">Remarks</span></span>

<span data-ttu-id="e1a17-120">時間軸中的每個物件最多隻能有一個音量信封效果。</span><span class="sxs-lookup"><span data-stu-id="e1a17-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="e1a17-121">在組合或群組中，會先套用音量信封，再套用任何其他音訊效果，而不論其優先順序為何。</span><span class="sxs-lookup"><span data-stu-id="e1a17-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="e1a17-122">在來源或播放軌中，會根據其優先順序套用磁片區效果。</span><span class="sxs-lookup"><span data-stu-id="e1a17-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



