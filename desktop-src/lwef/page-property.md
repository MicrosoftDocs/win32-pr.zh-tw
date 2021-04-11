---
title: 頁面屬性
description: 頁面屬性
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372172"
---
# <a name="page-property"></a><span data-ttu-id="eef7d-103">頁面屬性</span><span class="sxs-lookup"><span data-stu-id="eef7d-103">Page Property</span></span>

<span data-ttu-id="eef7d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="eef7d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eef7d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="eef7d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eef7d-106">傳回或設定顯示在 [Microsoft Agent 屬性工作表] 視窗中的頁面。</span><span class="sxs-lookup"><span data-stu-id="eef7d-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="eef7d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="eef7d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="eef7d-108">\*代理程式 \* \* *。PropertySheet.Page* \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="eef7d-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="eef7d-109">部分</span><span class="sxs-lookup"><span data-stu-id="eef7d-109">Part</span></span>     | <span data-ttu-id="eef7d-110">描述</span><span class="sxs-lookup"><span data-stu-id="eef7d-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef7d-111">*string*</span><span class="sxs-lookup"><span data-stu-id="eef7d-111">*string*</span></span> | <span data-ttu-id="eef7d-112">具有下列其中一個值的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="eef7d-112">A string expression with one of the following values.</span></span> <span data-ttu-id="eef7d-113">**"Speech"** 顯示 [語音輸入] 頁面。</span><span class="sxs-lookup"><span data-stu-id="eef7d-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="eef7d-114">**"Output"** 顯示 [輸出] 頁面。</span><span class="sxs-lookup"><span data-stu-id="eef7d-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="eef7d-115">**"著作權"** 顯示 [著作權] 頁面。</span><span class="sxs-lookup"><span data-stu-id="eef7d-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eef7d-116">備註</span><span class="sxs-lookup"><span data-stu-id="eef7d-116">Remarks</span></span>

<span data-ttu-id="eef7d-117">如果未安裝任何語音引擎，將 **頁面** 設定為 **"speech"** 沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="eef7d-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="eef7d-118">此外，視窗的 **Visible** 屬性必須設定為 **True** ，使用者才能看到該頁面。</span><span class="sxs-lookup"><span data-stu-id="eef7d-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="eef7d-119">使用者可以覆寫這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eef7d-119">The user can override this property.</span></span>

 

 

 





