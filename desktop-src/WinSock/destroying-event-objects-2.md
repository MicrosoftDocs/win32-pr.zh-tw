---
description: 當不再需要事件物件時，使用 WPUCloseEvent 終結事件物件 (應用程式或服務提供者) 。
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: 終結事件物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318392"
---
# <a name="destroying-event-objects"></a><span data-ttu-id="dcb35-103">終結事件物件</span><span class="sxs-lookup"><span data-stu-id="dcb35-103">Destroying Event Objects</span></span>

<span data-ttu-id="dcb35-104">建立事件物件 (應用程式或服務提供者) 的實體會在不再需要時，負責將它終結。</span><span class="sxs-lookup"><span data-stu-id="dcb35-104">The entity that creates an event object (application or service provider) is responsible for destroying it when it is no longer required.</span></span> <span data-ttu-id="dcb35-105">服務提供者透過 **WPUCloseEvent** 執行此動作。</span><span class="sxs-lookup"><span data-stu-id="dcb35-105">Service providers do this through **WPUCloseEvent**.</span></span>

 

 



