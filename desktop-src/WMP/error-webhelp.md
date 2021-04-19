---
title: WebHelp 方法
description: WebHelp 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。 |WebHelp 方法
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- webHelp 方法 Windows Media Player
- webHelp 方法 Windows Media Player，Error 類別
- Error 類別 Windows Media Player，webHelp 方法
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991165"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="c515d-107">WebHelp 方法</span><span class="sxs-lookup"><span data-stu-id="c515d-107">Error.webHelp method</span></span>

<span data-ttu-id="c515d-108">**WebHelp** 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。</span><span class="sxs-lookup"><span data-stu-id="c515d-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="c515d-109">語法</span><span class="sxs-lookup"><span data-stu-id="c515d-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="c515d-110">參數</span><span class="sxs-lookup"><span data-stu-id="c515d-110">Parameters</span></span>

<span data-ttu-id="c515d-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c515d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c515d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c515d-112">Return value</span></span>

<span data-ttu-id="c515d-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c515d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c515d-114">備註</span><span class="sxs-lookup"><span data-stu-id="c515d-114">Remarks</span></span>

<span data-ttu-id="c515d-115">Web 說明頁面一律包含 Windows Media Player 錯誤的最新和最詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="c515d-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="c515d-116">此方法會自動傳送 Web 說明所需的其他資訊，例如使用的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="c515d-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="c515d-117">若要直接存取 Web 說明頁面，請使用下列錯誤碼和支援中心連結。</span><span class="sxs-lookup"><span data-stu-id="c515d-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="c515d-118">Windows Media Player 錯誤碼資訊</span><span class="sxs-lookup"><span data-stu-id="c515d-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="c515d-119">Windows Media Player 解決方案中心</span><span class="sxs-lookup"><span data-stu-id="c515d-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="c515d-120">**Windows Media Player 10** 行動裝置版：這個方法一律會成功，但不會執行預定的作業。</span><span class="sxs-lookup"><span data-stu-id="c515d-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="c515d-121">範例</span><span class="sxs-lookup"><span data-stu-id="c515d-121">Examples</span></span>

<span data-ttu-id="c515d-122">下列範例會建立 HTML BUTTON 元素，以啟動 Microsoft Windows Media Player Web 說明頁面。</span><span class="sxs-lookup"><span data-stu-id="c515d-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="c515d-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c515d-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="c515d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c515d-124">Requirements</span></span>



| <span data-ttu-id="c515d-125">需求</span><span class="sxs-lookup"><span data-stu-id="c515d-125">Requirement</span></span> | <span data-ttu-id="c515d-126">值</span><span class="sxs-lookup"><span data-stu-id="c515d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c515d-127">版本</span><span class="sxs-lookup"><span data-stu-id="c515d-127">Version</span></span><br/> | <span data-ttu-id="c515d-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c515d-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c515d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c515d-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c515d-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c515d-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c515d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c515d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c515d-132">**Error 物件**</span><span class="sxs-lookup"><span data-stu-id="c515d-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





