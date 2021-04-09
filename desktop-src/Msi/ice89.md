---
description: ICE89 會驗證 progid 資料表中 Progid 父資料行中的值， \_ 是否為 progid 資料表中 progid 資料行的有效外鍵。 每個 ProgId 父代都應該在 ProgId 資料表中有一筆記錄。
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944977"
---
# <a name="ice89"></a><span data-ttu-id="1f34c-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="1f34c-104">ICE89</span></span>

<span data-ttu-id="1f34c-105">ICE89 會驗證 progid 資料表中 Progid 父資料行中的值， \_ 是否為 progid 資料表中 progid 資料行的有效外鍵。 [](progid-table.md)</span><span class="sxs-lookup"><span data-stu-id="1f34c-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="1f34c-106">每個 ProgId 父代都應該在 ProgId 資料表中有一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="1f34c-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="1f34c-107">結果</span><span class="sxs-lookup"><span data-stu-id="1f34c-107">Result</span></span>

<span data-ttu-id="1f34c-108">ICE89 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="1f34c-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="1f34c-109">ICE89 錯誤</span><span class="sxs-lookup"><span data-stu-id="1f34c-109">ICE89 error</span></span>                                                           | <span data-ttu-id="1f34c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1f34c-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="1f34c-111">\_Progid 資料表中的 progid 父項 ' \[ 1 \] ' 不是有效的 progid。</span><span class="sxs-lookup"><span data-stu-id="1f34c-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="1f34c-112">ProgId 資料表中未列出指定的 ProgId 父代。</span><span class="sxs-lookup"><span data-stu-id="1f34c-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1f34c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f34c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f34c-114">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="1f34c-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



