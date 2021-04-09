---
title: 音量標記
description: 音量標記
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021002"
---
# <a name="vol-tag"></a><span data-ttu-id="2365f-103">音量標記</span><span class="sxs-lookup"><span data-stu-id="2365f-103">Vol Tag</span></span>

<span data-ttu-id="2365f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2365f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2365f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="2365f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2365f-106">設定語音輸出的基準說話量。</span><span class="sxs-lookup"><span data-stu-id="2365f-106">Sets the baseline speaking volume of the speech output.</span></span>

</dd> <dt>

<span data-ttu-id="2365f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="2365f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2365f-108">**\\音量 =***數位***\\**</span><span class="sxs-lookup"><span data-stu-id="2365f-108">**\\Vol=***number***\\**</span></span>



| <span data-ttu-id="2365f-109">部分</span><span class="sxs-lookup"><span data-stu-id="2365f-109">Part</span></span>     | <span data-ttu-id="2365f-110">描述</span><span class="sxs-lookup"><span data-stu-id="2365f-110">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="2365f-111">*number*</span><span class="sxs-lookup"><span data-stu-id="2365f-111">*number*</span></span> | <span data-ttu-id="2365f-112">基準朗讀磁片區：0是無回應，而65535是最大音量。</span><span class="sxs-lookup"><span data-stu-id="2365f-112">Baseline speaking volume: 0 is silence and 65535 is maximum volume.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="2365f-113">備註</span><span class="sxs-lookup"><span data-stu-id="2365f-113">Remarks</span></span>

<span data-ttu-id="2365f-114">[磁片區] 設定會影響左右通道。</span><span class="sxs-lookup"><span data-stu-id="2365f-114">The volume setting affects both left and right channels.</span></span> <span data-ttu-id="2365f-115">您無法分別設定每個通道的音量。</span><span class="sxs-lookup"><span data-stu-id="2365f-115">You cannot set the volume of each channel separately.</span></span> <span data-ttu-id="2365f-116">只有 TTS 產生的輸出才支援此標記。</span><span class="sxs-lookup"><span data-stu-id="2365f-116">This tag is supported only for TTS-generated output.</span></span>

 

 




