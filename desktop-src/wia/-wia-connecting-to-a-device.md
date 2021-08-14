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
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451218"
---
# <a name="connecting-to-a-device"></a>連接至裝置

> [!Note]  
> 此腳本系統已取代為 Windows 的影像取得 (WIA) Automation 層。 請參閱[Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

 

任何使用 Windows 影像取得的應用程式或腳本中的第一個步驟 (wia) 腳本模型正在建立 [**WIA**](-wia-wia.md)物件。 這個物件會提供方法，以取得 [**DeviceInfo**](-wia-deviceinfo.md) 物件的集合，並將這些物件連接至裝置。 它也提供接聽 WIA 硬體事件的能力。

下列 Microsoft Visual Basic 腳本版本 (VBScript) 程式碼建立 [**Wia**](-wia-wia.md)物件：


```
objWia = CreateObject("Wia.Script")
```



建立 [**wia**](-wia-wia.md) 物件之後，請使用其 [**Create**](-wia-iwia-create.md) 方法來連接至 Wia 硬體裝置。

您也可以使用 [**Wia**](-wia-wia.md) 物件的 [ [**裝置**](-wia-iwia-devices.md) ] 屬性來取得 [**DeviceInfo**](-wia-deviceinfo.md) 物件的集合。 列舉此集合，並使用 [**Create**](-wia-iwiadeviceinfo-create.md) 方法來連接至裝置。

 

 
