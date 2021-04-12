---
description: 裝置上的 Web 服務會使用下列常數。
ms.assetid: ef3df24a-46a1-49de-b2f7-bfccdc793462
title: '裝置上的 Web 服務常數 (Wsdutil .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984946df757e059ef667b94274818aa2b38c87f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192902"
---
# <a name="web-services-on-devices-constants"></a>裝置上的 Web 服務常數

裝置上的 Web 服務會使用下列常數。



| 常數                                                                                                                                                                                                                        | 描述                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WSD_DEFAULT_HOSTING_ADDRESS"></span><span id="wsd_default_hosting_address"></span><dl> <dt>**WSD \_ 預設 \_ 主機 \_ 位址**</dt> </dl>                       | 預設位址 ([UrlPrefix](/windows/desktop/Http/urlprefix-strings) 格式) ，WSDAPI 主機會使用此格式接聽埠5357上的要求。 <br/>                                                 |
| <span id="WSD_DEFAULT_SECURE_HOSTING_ADDRESS"></span><span id="wsd_default_secure_hosting_address"></span><dl> <dt>**WSD \_ 預設 \_ 安全 \_ 裝載 \_ 位址**</dt> </dl> | 預設安全位址 (為 [UrlPrefix](/windows/desktop/Http/urlprefix-strings) 格式) ，WSDAPI 主機會使用此格式接聽埠5358上的要求。 <br/>                                          |
| <span id="WSD_DEFAULT_EVENTING_ADDRESS__"></span><span id="wsd_default_eventing_address__"></span><dl> <dt>**WSD \_預設 \_ 事件 \_ 處理位址**</dt> </dl>               | 預設位址 (為 [UrlPrefix](/windows/desktop/Http/urlprefix-strings) 格式) ，WSDAPI 主機會使用此格式來接聽埠5358上的安全主機和埠5357上的事件（適用于其他主機）。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wsdutil。h</dt> </dl> |



 

