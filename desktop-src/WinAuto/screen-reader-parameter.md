---
title: 螢幕讀取器參數
description: 螢幕讀取器參數會指出應用程式是否應該在以圖形方式呈現資訊的情況下，提供文字資訊。
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023748"
---
# <a name="screen-reader-parameter"></a><span data-ttu-id="08968-103">螢幕讀取器參數</span><span class="sxs-lookup"><span data-stu-id="08968-103">Screen reader parameter</span></span>

<span data-ttu-id="08968-104">螢幕讀取器參數會指出應用程式是否應該在以圖形方式呈現資訊的情況下，提供文字資訊。</span><span class="sxs-lookup"><span data-stu-id="08968-104">The screen reader parameter indicates whether an application should provide textual information in situations where it would otherwise present the information graphically.</span></span>

<span data-ttu-id="08968-105">此參數通常是由協助工具協助工具（例如螢幕讀取器）設定。</span><span class="sxs-lookup"><span data-stu-id="08968-105">This parameter is typically set by accessibility aids such as screen readers.</span></span> <span data-ttu-id="08968-106">應用程式會使用 **spi \_ GETSCREENREADER** 和 **spi \_ SETSCREENREADER** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定螢幕讀取器參數。</span><span class="sxs-lookup"><span data-stu-id="08968-106">Applications use the **SPI\_GETSCREENREADER** and **SPI\_SETSCREENREADER** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the screen reader parameter.</span></span>

> [!Note]  
> <span data-ttu-id="08968-107">[朗讀程式] 是 Windows 隨附的螢幕讀取器，並不會設定 **spi \_ SETSCREENREADER** 或 **spi \_ GETSCREENREADER** 旗標。</span><span class="sxs-lookup"><span data-stu-id="08968-107">Narrator, the screen reader that is included with Windows, does not set the **SPI\_SETSCREENREADER** or **SPI\_GETSCREENREADER** flags.</span></span>

 

 

 