---
title: 什麼是控制點物件模型
description: 下圖顯示基本控制點物件模型。
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311361"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="66013-103">什麼是控制點物件模型？</span><span class="sxs-lookup"><span data-stu-id="66013-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="66013-104">下圖顯示基本控制點物件模型。</span><span class="sxs-lookup"><span data-stu-id="66013-104">The following illustration shows the basic Control Point object model.</span></span>

![控制點物件模型](images/upnp-object-model.png)

<span data-ttu-id="66013-106">使用裝置搜尋工具來搜尋裝置會建立裝置集合。</span><span class="sxs-lookup"><span data-stu-id="66013-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="66013-107">裝置集合包含零或多個裝置物件。</span><span class="sxs-lookup"><span data-stu-id="66013-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="66013-108">應用程式可以使用各種裝置集合方法來存取個別的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="66013-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="66013-109">裝置物件一律會包含包含一或多個服務物件的服務集合。</span><span class="sxs-lookup"><span data-stu-id="66013-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="66013-110">應用程式會使用這些服務物件來與裝置通訊及控制裝置。</span><span class="sxs-lookup"><span data-stu-id="66013-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 




