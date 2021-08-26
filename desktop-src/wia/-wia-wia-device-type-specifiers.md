---
description: Windows影像取得 (WIA) 裝置類型規範是指出附加至使用者電腦之裝置類型的常數。
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: WIA 裝置類型規範
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdefac4672b46fea7a7dad021fa9ebec710b3b77eabb7a1f7cac405b8e7e519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056968"
---
# <a name="wia-device-type-specifiers"></a>WIA 裝置類型規範

Windows影像取得 (WIA) 裝置類型規範是指出附加至使用者電腦之裝置類型的常數。 使用 GET \_ STIDEVICE \_ TYPE 宏從 WIA 裝置類型屬性取得這些值。 以下是有效的 WIA 裝置類型規範： 

| 裝置類型                 | 意義                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | 一般 WIA 裝置。 在裝置列舉期間，會使用這個常數來列舉所有的 WIA 裝置。                         |
| StiDeviceTypeDigitalCamera  | 裝置是相機。 Windows Vista *和更新版本**不支援此規範*。                                     |
| StiDeviceTypeScanner        | 裝置是掃描器。                                                                                                    |
| StiDeviceTypeStreamingVideo | 裝置包含串流影片。 Windows Server 2003 *、* Windows Vista *或更新版本**不支援此規範*。 |



 

 

 



