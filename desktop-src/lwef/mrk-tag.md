---
title: Mrk 標記
description: Mrk 標記
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673207"
---
# <a name="mrk-tag"></a><span data-ttu-id="94df1-103">Mrk 標記</span><span class="sxs-lookup"><span data-stu-id="94df1-103">Mrk Tag</span></span>

<span data-ttu-id="94df1-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="94df1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="94df1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="94df1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="94df1-106">定義說出文字中的書簽。</span><span class="sxs-lookup"><span data-stu-id="94df1-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="94df1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="94df1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="94df1-108">**\\Mrk =***數位***\\**</span><span class="sxs-lookup"><span data-stu-id="94df1-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="94df1-109">部分</span><span class="sxs-lookup"><span data-stu-id="94df1-109">Part</span></span>     | <span data-ttu-id="94df1-110">描述</span><span class="sxs-lookup"><span data-stu-id="94df1-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="94df1-111">*number*</span><span class="sxs-lookup"><span data-stu-id="94df1-111">*number*</span></span> | <span data-ttu-id="94df1-112">識別書簽的長整數值。</span><span class="sxs-lookup"><span data-stu-id="94df1-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="94df1-113">備註</span><span class="sxs-lookup"><span data-stu-id="94df1-113">Remarks</span></span>

<span data-ttu-id="94df1-114">當伺服器處理書簽時，會產生書簽事件。</span><span class="sxs-lookup"><span data-stu-id="94df1-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="94df1-115">您必須指定大於零的數位 (0) 且不等於2147483647或2147483646。</span><span class="sxs-lookup"><span data-stu-id="94df1-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




