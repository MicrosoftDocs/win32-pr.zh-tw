---
title: Ctx 標記
description: Ctx 標記
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021688"
---
# <a name="ctx-tag"></a><span data-ttu-id="9d572-103">Ctx 標記</span><span class="sxs-lookup"><span data-stu-id="9d572-103">Ctx Tag</span></span>

<span data-ttu-id="9d572-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9d572-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9d572-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="9d572-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9d572-106">設定輸出文字的內容。</span><span class="sxs-lookup"><span data-stu-id="9d572-106">Sets the context of the output text.</span></span>

</dd> <dt>

<span data-ttu-id="9d572-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="9d572-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9d572-108">\\**Ctx** =*字串*</span><span class="sxs-lookup"><span data-stu-id="9d572-108">\\**Ctx**=*string*</span></span>\\



| <span data-ttu-id="9d572-109">部分</span><span class="sxs-lookup"><span data-stu-id="9d572-109">Part</span></span>     | <span data-ttu-id="9d572-110">描述</span><span class="sxs-lookup"><span data-stu-id="9d572-110">Description</span></span>                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d572-111">*string*</span><span class="sxs-lookup"><span data-stu-id="9d572-111">*string*</span></span> | <span data-ttu-id="9d572-112">字串，指定下文字的內容，以決定如何說出符號或縮寫。</span><span class="sxs-lookup"><span data-stu-id="9d572-112">A string specifying the context of the text that follows, which determines how symbols or abbreviations are spoken.</span></span><br/> <span data-ttu-id="9d572-113">**"Address"**    位址和/或電話號碼。</span><span class="sxs-lookup"><span data-stu-id="9d572-113">**"Address"**    Addresses and/or phone numbers.</span></span><br/> <span data-ttu-id="9d572-114">「**電子郵件**」   電子郵件。</span><span class="sxs-lookup"><span data-stu-id="9d572-114">**"E-mail"**    Electronic mail.</span></span><br/> <span data-ttu-id="9d572-115">「**未知**」 (預設) 內容不明。</span><span class="sxs-lookup"><span data-stu-id="9d572-115">**"Unknown"**    (Default) Context is unknown.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9d572-116">備註</span><span class="sxs-lookup"><span data-stu-id="9d572-116">Remarks</span></span>

<span data-ttu-id="9d572-117">只有 TTS 產生的輸出才支援此標記。</span><span class="sxs-lookup"><span data-stu-id="9d572-117">This tag is supported only for TTS-generated output.</span></span> <span data-ttu-id="9d572-118">參數的值範圍可能會根據已安裝的 TTS 引擎而有所不同。</span><span class="sxs-lookup"><span data-stu-id="9d572-118">The range of values for the parameter may vary depending on the installed TTS engine.</span></span>

 

 





