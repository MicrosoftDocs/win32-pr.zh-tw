---
title: 關於操縱杆
description: 關於操縱杆
ms.assetid: 0cfff45b-48d4-4e0c-addf-e131d3a31187
keywords:
- Windows 多媒體，操縱杆
- 多媒體、操縱杆
- 多媒體輸入，操縱杆
- 操縱杆，關於
- 操縱杆、雙軸移動
- 操縱杆，三軸移動
- 操縱杆，按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a5b2c890e64e397887d89eb5d632b6c4b63689
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021112"
---
# <a name="about-joysticks"></a><span data-ttu-id="b3966-110">關於操縱杆</span><span class="sxs-lookup"><span data-stu-id="b3966-110">About Joysticks</span></span>

<span data-ttu-id="b3966-111">搖桿是適用于應用程式的輔助輸入裝置，可提供使用鍵盤和滑鼠的替代方案。</span><span class="sxs-lookup"><span data-stu-id="b3966-111">The joystick is an ancillary input device for applications that provide alternatives to using the keyboard and mouse.</span></span> <span data-ttu-id="b3966-112">搖桿會在座標系統內提供位置資訊，此座標系統中的每個移動軸都有絕對的最大值和最小值。</span><span class="sxs-lookup"><span data-stu-id="b3966-112">The joystick provides positional information within a coordinate system that has absolute maximum and minimum values in each axis of movement.</span></span>

<span data-ttu-id="b3966-113">當作業系統啟動時，會載入搖桿服務。</span><span class="sxs-lookup"><span data-stu-id="b3966-113">Joystick services are loaded when the operating system is started.</span></span> <span data-ttu-id="b3966-114">搖桿服務可以同時監視兩個搖桿，各有兩個或三個軸的移動。</span><span class="sxs-lookup"><span data-stu-id="b3966-114">The joystick services can simultaneously monitor two joysticks, each with two- or three-axis movement.</span></span> <span data-ttu-id="b3966-115">每個搖桿最多可有四個按鈕。</span><span class="sxs-lookup"><span data-stu-id="b3966-115">Each joystick can have up to four buttons.</span></span> <span data-ttu-id="b3966-116">您可以使用搖桿功能來判斷搖桿和搖桿驅動程式的功能。</span><span class="sxs-lookup"><span data-stu-id="b3966-116">You can use the joystick functions to determine the capabilities of the joysticks and joystick driver.</span></span> <span data-ttu-id="b3966-117">此外，您也可以直接查詢操縱杆，或藉由捕捉搖桿和處理訊息，來處理搖桿的位置和按鈕資訊。</span><span class="sxs-lookup"><span data-stu-id="b3966-117">Also, you can process a joystick's positional and button information by querying the joystick directly or by capturing the joystick and processing messages from it.</span></span> <span data-ttu-id="b3966-118">第二種方法比較簡單，因為您的應用程式不需要手動查詢搖桿，也不需要追蹤時間定期產生查詢。</span><span class="sxs-lookup"><span data-stu-id="b3966-118">The latter method is simpler because your application does not have to manually query the joystick or track the time to generate queries at regular intervals.</span></span>

 

 




