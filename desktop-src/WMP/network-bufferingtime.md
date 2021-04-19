---
title: BufferingTime
description: BufferingTime 屬性會指定或抓取在開始播放之前，為了緩衝處理傳入資料所配置的時間量（以毫秒為單位）。
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- BufferingTime Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997645"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="fafe5-104">BufferingTime</span><span class="sxs-lookup"><span data-stu-id="fafe5-104">Network.bufferingTime</span></span>

<span data-ttu-id="fafe5-105">**BufferingTime** 屬性會指定或抓取在開始播放之前，為了緩衝處理傳入資料所配置的時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fafe5-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafe5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fafe5-106">Syntax</span></span>

<span data-ttu-id="fafe5-107">*玩家*。*網路*。**bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="fafe5-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fafe5-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="fafe5-108">Possible Values</span></span>

<span data-ttu-id="fafe5-109">此屬性是讀取/寫入 **號碼** (**長**) 範圍從零到60000，預設值是5000。</span><span class="sxs-lookup"><span data-stu-id="fafe5-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="fafe5-110">範例</span><span class="sxs-lookup"><span data-stu-id="fafe5-110">Examples</span></span>

<span data-ttu-id="fafe5-111">下列 JScript 範例會使用 *網路*。**bufferingTime** ，指定配置給緩衝傳入資料的秒數。</span><span class="sxs-lookup"><span data-stu-id="fafe5-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="fafe5-112">系統會從以 ID = "bufText" 建立的 HTML 文字輸入元素抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="fafe5-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="fafe5-113">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="fafe5-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="fafe5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fafe5-114">Requirements</span></span>



| <span data-ttu-id="fafe5-115">需求</span><span class="sxs-lookup"><span data-stu-id="fafe5-115">Requirement</span></span> | <span data-ttu-id="fafe5-116">值</span><span class="sxs-lookup"><span data-stu-id="fafe5-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fafe5-117">版本</span><span class="sxs-lookup"><span data-stu-id="fafe5-117">Version</span></span><br/> | <span data-ttu-id="fafe5-118">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fafe5-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fafe5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fafe5-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="fafe5-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafe5-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fafe5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fafe5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafe5-122">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="fafe5-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





