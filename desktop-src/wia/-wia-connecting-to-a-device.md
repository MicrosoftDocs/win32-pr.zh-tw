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
# <a name="connecting-to-a-device"></a>連接至裝置

> [!Note]  
> 此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。 請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

 

任何使用 Windows 映像取得的應用程式或腳本中的第一個步驟 (WIA) 腳本模型正在建立 [**WIA**](-wia-wia.md) 物件。 這個物件會提供方法，以取得 [**DeviceInfo**](-wia-deviceinfo.md) 物件的集合，並將這些物件連接至裝置。 它也提供接聽 WIA 硬體事件的能力。

下列這一行 Microsoft Visual Basic Scripting Edition (VBScript) 程式碼建立 [**Wia**](-wia-wia.md) 物件：


```
objWia = CreateObject("Wia.Script")
```



建立 [**wia**](-wia-wia.md) 物件之後，請使用其 [**Create**](-wia-iwia-create.md) 方法來連接至 Wia 硬體裝置。

您也可以使用 [**Wia**](-wia-wia.md) 物件的 [ [**裝置**](-wia-iwia-devices.md) ] 屬性來取得 [**DeviceInfo**](-wia-deviceinfo.md) 物件的集合。 列舉此集合，並使用 [**Create**](-wia-iwiadeviceinfo-create.md) 方法來連接至裝置。

 

 
