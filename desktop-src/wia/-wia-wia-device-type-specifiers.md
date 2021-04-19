---
description: Windows 映像取得 (WIA) 裝置類型規範是指出附加至使用者電腦之裝置類型的常數。
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: WIA 裝置類型規範
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997492"
---
# <a name="wia-device-type-specifiers"></a>WIA 裝置類型規範

Windows 映像取得 (WIA) 裝置類型規範是指出附加至使用者電腦之裝置類型的常數。 使用 GET \_ STIDEVICE \_ TYPE 宏從 WIA 裝置類型屬性取得這些值。 以下是有效的 WIA 裝置類型規範： 

| 裝置類型                 | 意義                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | 一般 WIA 裝置。 在裝置列舉期間，會使用這個常數來列舉所有的 WIA 裝置。                         |
| StiDeviceTypeDigitalCamera  | 裝置是相機。 *不支援這個規範* Windows Vista （含） *以後版本。*                                     |
| StiDeviceTypeScanner        | 裝置是掃描器。                                                                                                    |
| StiDeviceTypeStreamingVideo | 裝置包含串流影片。 *不支援這個規範* Windows Server 2003 *、* windows Vista *或更新版本。* |



 

 

 



