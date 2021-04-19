---
description: 抓取 Windows 映像取得 (WIA) 硬體裝置的類型。
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo。 Type 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972465"
---
# <a name="deviceinfotype-property"></a>DeviceInfo。 Type 屬性

抓取 Windows 映像取得 (WIA) 硬體裝置的類型。 可能的值包括：

-   DigitalCamera
-   掃描器
-   StreamingVideo
-   預設

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>屬性值

接收裝置的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




