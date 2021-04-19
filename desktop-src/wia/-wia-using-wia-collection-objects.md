---
description: 「集合」（collection）是包含一個或多個物件的物件。 集合提供有效率的方式來分組類似的物件。 Windows 映像取得 (WIA) 提供 DeviceInfo 和 Item 物件的集合。
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: 使用 WIA 集合物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972865"
---
# <a name="using-wia-collection-objects"></a>使用 WIA 集合物件

「集合」（collection）是包含一個或多個物件的物件。 集合提供有效率的方式來分組類似的物件。 Windows 映像取得 (WIA) 提供 [**DeviceInfo**](-wia-deviceinfo.md) 和 [**Item**](-wia-item.md) 物件的集合。

使用集合來列舉它們所包含的物件。 例如，下列 VBScript 範例會從 [**Devices**](-wia-iwia-devices.md)方法取得 [**DeviceInfo**](-wia-deviceinfo.md)物件的集合，然後使用 **For .。。逐一** 查看集合的每個迴圈：


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> WIA 集合物件是以0為基礎。

 

 

 



