---
title: LaunchURL 方法
description: LaunchURL 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。 |LaunchURL 方法
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- launchURL 方法 Windows Media Player
- launchURL 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，launchURL 方法
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990550"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="b3092-107">LaunchURL 方法</span><span class="sxs-lookup"><span data-stu-id="b3092-107">Player.launchURL method</span></span>

<span data-ttu-id="b3092-108">**LaunchURL** 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。</span><span class="sxs-lookup"><span data-stu-id="b3092-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3092-109">語法</span><span class="sxs-lookup"><span data-stu-id="b3092-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="b3092-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3092-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3092-111">*URL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3092-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3092-112">表示要啟動之 URL 的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="b3092-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3092-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3092-113">Return value</span></span>

<span data-ttu-id="b3092-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b3092-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3092-115">備註</span><span class="sxs-lookup"><span data-stu-id="b3092-115">Remarks</span></span>

<span data-ttu-id="b3092-116">這個方法只會使用 HTTP 或 HTTPS 通訊協定來開啟網頁。</span><span class="sxs-lookup"><span data-stu-id="b3092-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="b3092-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b3092-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="b3092-118">範例</span><span class="sxs-lookup"><span data-stu-id="b3092-118">Examples</span></span>

<span data-ttu-id="b3092-119">下列範例會建立 HTML BUTTON 元素，當按一下此專案時，會在新的瀏覽器視窗中顯示 Microsoft 網站。</span><span class="sxs-lookup"><span data-stu-id="b3092-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="b3092-120">**播放** 程式元素是以 ID = "Player" 建立。</span><span class="sxs-lookup"><span data-stu-id="b3092-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="b3092-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3092-121">Requirements</span></span>



| <span data-ttu-id="b3092-122">需求</span><span class="sxs-lookup"><span data-stu-id="b3092-122">Requirement</span></span> | <span data-ttu-id="b3092-123">值</span><span class="sxs-lookup"><span data-stu-id="b3092-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3092-124">版本</span><span class="sxs-lookup"><span data-stu-id="b3092-124">Version</span></span><br/> | <span data-ttu-id="b3092-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b3092-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3092-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b3092-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3092-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3092-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3092-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3092-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3092-129">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="b3092-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





