---
description: 下列錯誤碼適用于安裝程式 API。
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: " (設定 API) 的錯誤碼"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469353"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="52de1-103"> (設定 API) 的錯誤碼</span><span class="sxs-lookup"><span data-stu-id="52de1-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="52de1-104">下列錯誤碼適用于安裝程式 API。</span><span class="sxs-lookup"><span data-stu-id="52de1-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="52de1-105">INF 剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="52de1-105">INF Parsing Errors</span></span>              | <span data-ttu-id="52de1-106">Description</span><span class="sxs-lookup"><span data-stu-id="52de1-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52de1-107">錯誤的 \_ 預期 \_ 區段 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="52de1-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="52de1-108">需要區段名稱，但找不到。</span><span class="sxs-lookup"><span data-stu-id="52de1-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="52de1-109">錯誤 \_ 的 \_ 區段 \_ 名稱 \_ 行</span><span class="sxs-lookup"><span data-stu-id="52de1-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="52de1-110">區段名稱的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="52de1-110">The section name was not of the correct format.</span></span> <span data-ttu-id="52de1-111">例如， (不是由右括弧結束的名稱 ( \] ) 。</span><span class="sxs-lookup"><span data-stu-id="52de1-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="52de1-112">錯誤 \_ 區段 \_ 名稱 \_ 太 \_ 長</span><span class="sxs-lookup"><span data-stu-id="52de1-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="52de1-113">區段名稱超過最大 \_ 區段名稱 LEN 的最大長度 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="52de1-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="52de1-114">錯誤 \_ 一般 \_ 語法</span><span class="sxs-lookup"><span data-stu-id="52de1-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="52de1-115">一般語法不正確。</span><span class="sxs-lookup"><span data-stu-id="52de1-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="52de1-116">INF 執行階段錯誤</span><span class="sxs-lookup"><span data-stu-id="52de1-116">INF Runtime Errors</span></span>         | <span data-ttu-id="52de1-117">Description</span><span class="sxs-lookup"><span data-stu-id="52de1-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52de1-118">錯誤 \_ 的 \_ INF \_ 樣式錯誤</span><span class="sxs-lookup"><span data-stu-id="52de1-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="52de1-119">INF 檔案不是函式呼叫中所指定的類型。</span><span class="sxs-lookup"><span data-stu-id="52de1-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="52de1-120">例如，如果 INF 檔案是針對早期版本的 Windows 所設計，則 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) 函式可能會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="52de1-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="52de1-121">\_ \_ 找不到錯誤區段 \_</span><span class="sxs-lookup"><span data-stu-id="52de1-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="52de1-122">INF 檔案中找不到區段。</span><span class="sxs-lookup"><span data-stu-id="52de1-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="52de1-123">\_ \_ 找不到錯誤行 \_</span><span class="sxs-lookup"><span data-stu-id="52de1-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="52de1-124">在 INF 區段中找不到該行。</span><span class="sxs-lookup"><span data-stu-id="52de1-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



