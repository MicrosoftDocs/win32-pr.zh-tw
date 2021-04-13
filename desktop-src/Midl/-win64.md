---
title: /win64 參數
description: /Win64 參數會指示 MIDL 編譯器產生64位環境的存根檔或類型程式庫檔案。請注意，此參數已淘汰。
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /win64 參數 MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312297"
---
# <a name="win64-switch"></a><span data-ttu-id="f14cb-104">/win64 參數</span><span class="sxs-lookup"><span data-stu-id="f14cb-104">/win64 switch</span></span>

<span data-ttu-id="f14cb-105">**/Win64** 參數會指示 MIDL 編譯器產生64位環境的存根檔或類型程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="f14cb-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="f14cb-106">此參數已淘汰。</span><span class="sxs-lookup"><span data-stu-id="f14cb-106">This switch is obsolete.</span></span> <span data-ttu-id="f14cb-107">請改用 [**/ia64**](-ia64.md) 或 [**/amd64**](-amd64.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="f14cb-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="f14cb-108">**/Win64** 參數相當於 **/ia64** 參數。</span><span class="sxs-lookup"><span data-stu-id="f14cb-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="f14cb-109">切換選項</span><span class="sxs-lookup"><span data-stu-id="f14cb-109">Switch Options</span></span>

<span data-ttu-id="f14cb-110">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f14cb-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f14cb-111">備註</span><span class="sxs-lookup"><span data-stu-id="f14cb-111">Remarks</span></span>

<span data-ttu-id="f14cb-112">**/Win64** 參數相當於將 [**/env**](-env.md)參數設定為 win64。</span><span class="sxs-lookup"><span data-stu-id="f14cb-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="f14cb-113">您無法使用 MIDL.exe 在 Windows 2000 上產生64位 tlb。</span><span class="sxs-lookup"><span data-stu-id="f14cb-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f14cb-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f14cb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14cb-115">**/env**</span><span class="sxs-lookup"><span data-stu-id="f14cb-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="f14cb-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="f14cb-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="f14cb-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="f14cb-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 




