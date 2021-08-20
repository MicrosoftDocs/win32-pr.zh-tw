---
description: 抓取 Windows 的映射取得類型 (WIA) 硬體裝置。
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
ms.openlocfilehash: 841ba87b71f79d1f9dfbf85053d914315f89f592ec16a50bd9f6baf061b989a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035499"
---
# <a name="deviceinfotype-property"></a>DeviceInfo。 Type 屬性

抓取 Windows 的映射取得類型 (WIA) 硬體裝置。 可能的值包括：

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
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




