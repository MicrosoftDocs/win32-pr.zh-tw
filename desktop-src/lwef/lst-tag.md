---
title: .Lst 標記
description: .Lst 標記
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507221"
---
# <a name="lst-tag"></a><span data-ttu-id="c3b78-103">.Lst 標記</span><span class="sxs-lookup"><span data-stu-id="c3b78-103">Lst Tag</span></span>

<span data-ttu-id="c3b78-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c3b78-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c3b78-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="c3b78-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c3b78-106">針對字元重複最後一個讀出的語句。</span><span class="sxs-lookup"><span data-stu-id="c3b78-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="c3b78-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="c3b78-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c3b78-108">\\**Lst**</span><span class="sxs-lookup"><span data-stu-id="c3b78-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="c3b78-109">備註</span><span class="sxs-lookup"><span data-stu-id="c3b78-109">Remarks</span></span>

<span data-ttu-id="c3b78-110">此標記可讓字元重複其最後一個讀出的語句。</span><span class="sxs-lookup"><span data-stu-id="c3b78-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="c3b78-111">這個標記必須單獨出現在 [**說話**](speak-method.md) 方法中;不能包含任何其他文字或參數。</span><span class="sxs-lookup"><span data-stu-id="c3b78-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="c3b78-112">當說出文字重複時，原始文字中包含的任何其他標記都會重複，除了書簽以外。</span><span class="sxs-lookup"><span data-stu-id="c3b78-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="c3b78-113">任何。WAV 和。文字中包含的 LWV 檔也會重複。</span><span class="sxs-lookup"><span data-stu-id="c3b78-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




