---
title: /no_format_opt 參數
description: /No \_ 格式 \_ 選擇參數會變更 MIDL 優化類型和程式描述項的方式。
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt switch MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106979657"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="0b30d-104">/no \_ 格式 \_ 選擇參數</span><span class="sxs-lookup"><span data-stu-id="0b30d-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="0b30d-105">**/No \_ 格式 \_ 選擇** 參數會變更 MIDL 優化類型和程式描述項的方式。</span><span class="sxs-lookup"><span data-stu-id="0b30d-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="0b30d-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="0b30d-106">Switch Options</span></span>

<span data-ttu-id="0b30d-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0b30d-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b30d-108">備註</span><span class="sxs-lookup"><span data-stu-id="0b30d-108">Remarks</span></span>

<span data-ttu-id="0b30d-109">根據預設，MIDL 會排除重複的類型和程式描述項，以縮減產生的 stub 程式碼大小。</span><span class="sxs-lookup"><span data-stu-id="0b30d-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="0b30d-110">使用 **/no \_ 格式 \_ 選擇** 參數會關閉此優化行為。</span><span class="sxs-lookup"><span data-stu-id="0b30d-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="0b30d-111">範例</span><span class="sxs-lookup"><span data-stu-id="0b30d-111">Examples</span></span>

<span data-ttu-id="0b30d-112">**midl/no \_ 格式 \_ opt mylean .idl**</span><span class="sxs-lookup"><span data-stu-id="0b30d-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0b30d-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b30d-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b30d-114">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="0b30d-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0b30d-115">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="0b30d-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




