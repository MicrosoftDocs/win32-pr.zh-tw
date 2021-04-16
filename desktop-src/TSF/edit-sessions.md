---
title: 編輯工作階段
description: 當文字服務必須取得、修改或設定內容中的文字時，就必須要求編輯會話。
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- 文字服務架構 (TSF) 、編輯會話
- TSF (文字服務架構) 、編輯會話
- 文字服務，編輯會話
- 編輯工作階段 (edit session)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507424"
---
# <a name="edit-sessions"></a><span data-ttu-id="81150-107">編輯工作階段</span><span class="sxs-lookup"><span data-stu-id="81150-107">Edit Sessions</span></span>

<span data-ttu-id="81150-108">當文字服務必須取得、修改或設定內容中的文字時，就必須要求 *編輯會話*。</span><span class="sxs-lookup"><span data-stu-id="81150-108">When a text service must obtain, modify, or set text in a context, it must request an *edit session*.</span></span> <span data-ttu-id="81150-109">當要求編輯會話時，TSF 管理員會與目標內容的擁有者協商所要求之類型的檔鎖定。</span><span class="sxs-lookup"><span data-stu-id="81150-109">When an edit session is requested, the TSF manager negotiates with the owner of the target context for a document lock of the requested type.</span></span> <span data-ttu-id="81150-110">當授與檔鎖定時，TSF 管理員可讓文字服務在內容中讀取及/或寫入文字。</span><span class="sxs-lookup"><span data-stu-id="81150-110">When the document lock is granted, the TSF manager enables the text service to read and/or write text to or from the context.</span></span>

 

 




