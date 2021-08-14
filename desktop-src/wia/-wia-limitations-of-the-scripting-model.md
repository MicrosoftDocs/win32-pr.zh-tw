---
description: 深入瞭解：腳本模型的限制
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: 腳本模型的限制
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4a1b2dc25c1ea73fd9d793e4d3de1bff7c8193b04aadbe00796ca4a021791886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208060"
---
# <a name="limitations-of-the-scripting-model"></a>腳本模型的限制

> [!Note]  
> 此腳本系統已取代為 Windows 的影像取得 (WIA) Automation 層。 請參閱[Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

 

Windows 影像取得 (wia) 腳本模型會公開 WIA 功能的子集。 下表提供腳本模型的限制描述。 

| WIA 功能               | 腳本模型限制                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 隱藏使用者介面  | 無法隱藏設定裝置/傳輸屬性的使用者介面。                                                                                                                                                                                               |
| 設定屬性              | 無法將 (寫入) 任何裝置或專案屬性。                                                                                                                                                                                                                        |
| 註冊回呼事件 | 只能接收三個指定事件的通知： [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)、 [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)和 [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md)。 |
| 處理錯誤                 | 無法處理 WIA 錯誤。                                                                                                                                                                                                                                                |



 

 

 
