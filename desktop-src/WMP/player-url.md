---
title: Player. URL
description: URL 屬性會指定或抓取要播放之媒體專案的名稱。
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999197"
---
# <a name="playerurl"></a><span data-ttu-id="1e2b8-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="1e2b8-104">Player.URL</span></span>

<span data-ttu-id="1e2b8-105">**URL** 屬性會指定或抓取要播放之媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e2b8-106">Syntax</span></span>

<span data-ttu-id="1e2b8-107">*玩家* 。**URL**</span><span class="sxs-lookup"><span data-stu-id="1e2b8-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1e2b8-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="1e2b8-108">Possible Values</span></span>

<span data-ttu-id="1e2b8-109">這個屬性是沒有預設值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2b8-110">備註</span><span class="sxs-lookup"><span data-stu-id="1e2b8-110">Remarks</span></span>

<span data-ttu-id="1e2b8-111">這個屬性只能設定為安全性區域中的 URL，該 URL 的安全性區域與呼叫的程式或網頁的安全性區域相同或較不嚴格。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="1e2b8-112">如果使用功能變數名稱伺服器 (DNS) 名稱（而非 IP 位址）指定位址，則從防火牆後方開啟媒體專案的應用程式將會有較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="1e2b8-113">請勿從事件處理常式程式碼呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="1e2b8-114">呼叫 *Player*。來自事件處理常式的 **URL** 可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="1e2b8-115">範例</span><span class="sxs-lookup"><span data-stu-id="1e2b8-115">Examples</span></span>

<span data-ttu-id="1e2b8-116">下列範例會建立 HTML 文字輸入專案和 HTML 按鈕 input 元素。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="1e2b8-117">TEXT 元素可讓使用者輸入路徑來指定要播放的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="1e2b8-118">BUTTON 元素會執行開啟檔案的 JScript，並啟動 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="1e2b8-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="1e2b8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e2b8-120">Requirements</span></span>



| <span data-ttu-id="1e2b8-121">需求</span><span class="sxs-lookup"><span data-stu-id="1e2b8-121">Requirement</span></span> | <span data-ttu-id="1e2b8-122">值</span><span class="sxs-lookup"><span data-stu-id="1e2b8-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2b8-123">版本</span><span class="sxs-lookup"><span data-stu-id="1e2b8-123">Version</span></span><br/> | <span data-ttu-id="1e2b8-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1e2b8-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1e2b8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2b8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e2b8-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b8-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2b8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e2b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2b8-128">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="1e2b8-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





