---
title: 搖桿位置
description: 搖桿位置
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- 操縱杆、位置
- 操縱杆，按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185866"
---
# <a name="joystick-position"></a><span data-ttu-id="07961-105">搖桿位置</span><span class="sxs-lookup"><span data-stu-id="07961-105">Joystick Position</span></span>

<span data-ttu-id="07961-106">您可以使用 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 函式，查詢搖桿是否有位置和按鈕資訊。</span><span class="sxs-lookup"><span data-stu-id="07961-106">You can query a joystick for position and button information by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="07961-107">例如，應用程式可以查詢搖桿的基準位置值。</span><span class="sxs-lookup"><span data-stu-id="07961-107">For example, an application can query the joystick for baseline position values.</span></span> <span data-ttu-id="07961-108">在校正搖桿時，[操縱杆主控台] 屬性工作表會使用這項技術。</span><span class="sxs-lookup"><span data-stu-id="07961-108">The Joystick Control Panel property sheet uses this technique when calibrating the joystick.</span></span>

<span data-ttu-id="07961-109">您也可以使用 [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) 函式，查詢具有擴充功能的搖桿或其他裝置。</span><span class="sxs-lookup"><span data-stu-id="07961-109">You can also query a joystick or other device that has extended capabilities by using the [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

 

 