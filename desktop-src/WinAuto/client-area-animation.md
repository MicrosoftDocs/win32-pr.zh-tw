---
title: 用戶端區域動畫參數
description: 用戶端區域動畫旗標會指出使用者是否想要停用 UI 元素中的動畫。
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186092"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="71804-103">用戶端區域動畫參數</span><span class="sxs-lookup"><span data-stu-id="71804-103">Client area animation parameter</span></span>

<span data-ttu-id="71804-104">用戶端區域動畫參數會指出使用者是否想要停用 UI 元素中的動畫。</span><span class="sxs-lookup"><span data-stu-id="71804-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="71804-105">顯示功能（例如閃爍、閃爍、閃爍和移動內容）可能會在具有相片相關癲癇的使用者中造成 seizures。</span><span class="sxs-lookup"><span data-stu-id="71804-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="71804-106">此參數可讓您啟用或停用所有這類動畫。</span><span class="sxs-lookup"><span data-stu-id="71804-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="71804-107">應用程式會使用 **spi \_ GETCLIENTAREAANIMATION** 和 **spi \_ SETCLIENTAREAANIMATION** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式，來開啟或關閉用戶端區域動畫。</span><span class="sxs-lookup"><span data-stu-id="71804-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 