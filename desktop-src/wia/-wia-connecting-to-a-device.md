---
description: 深入瞭解：連接至裝置
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: 連接至裝置
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982439"
---
# <a name="connecting-to-a-device"></a><span data-ttu-id="eb7b2-103">連接至裝置</span><span class="sxs-lookup"><span data-stu-id="eb7b2-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="eb7b2-104">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="eb7b2-105">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="eb7b2-106">任何使用 Windows 映像取得的應用程式或腳本中的第一個步驟 (WIA) 腳本模型正在建立 [**WIA**](-wia-wia.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="eb7b2-107">這個物件會提供方法，以取得 [**DeviceInfo**](-wia-deviceinfo.md) 物件的集合，並將這些物件連接至裝置。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="eb7b2-108">它也提供接聽 WIA 硬體事件的能力。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="eb7b2-109">下列這一行 Microsoft Visual Basic Scripting Edition (VBScript) 程式碼建立 [**Wia**](-wia-wia.md) 物件：</span><span class="sxs-lookup"><span data-stu-id="eb7b2-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="eb7b2-110">建立 [**wia**](-wia-wia.md) 物件之後，請使用其 [**Create**](-wia-iwia-create.md) 方法來連接至 Wia 硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="eb7b2-111">您也可以使用 [**Wia**](-wia-wia.md) 物件的 [ [**裝置**](-wia-iwia-devices.md) ] 屬性來取得 [**DeviceInfo**](-wia-deviceinfo.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="eb7b2-112">列舉此集合，並使用 [**Create**](-wia-iwiadeviceinfo-create.md) 方法來連接至裝置。</span><span class="sxs-lookup"><span data-stu-id="eb7b2-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 
