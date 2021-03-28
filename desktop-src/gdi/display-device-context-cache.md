---
description: 系統會維護快取，顯示其用於通用、父視窗和視窗裝置內容的顯示裝置內容。
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: 顯示裝置內容快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991266"
---
# <a name="display-device-context-cache"></a><span data-ttu-id="2cdb9-103">顯示裝置內容快取</span><span class="sxs-lookup"><span data-stu-id="2cdb9-103">Display Device Context Cache</span></span>

<span data-ttu-id="2cdb9-104">系統會維護快取，顯示其用於通用、父視窗和視窗裝置內容的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="2cdb9-105">每當應用程式呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式時，系統就會從快取中抓取裝置內容;當應用程式後續呼叫 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 或 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函式時，系統會將 DC 傳回給快取。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="2cdb9-106">快取可保存的裝置內容數量沒有預先決定的限制;如果沒有可用的快取，系統會建立新的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="2cdb9-107">如此一來，應用程式一次可以有超過五個來自快取的作用中裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="2cdb9-108">不過，應用程式必須在使用之後繼續釋出這些裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="2cdb9-109">由於快取的新顯示裝置內容會在應用程式的堆積空間中配置，因此無法釋出裝置內容最後都會耗用所有可用的堆積空間。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="2cdb9-110">系統會在無法為新的裝置內容配置空間時傳回錯誤，以指出此失敗。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="2cdb9-111">與快取無關的其他函數也可能會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2cdb9-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 



