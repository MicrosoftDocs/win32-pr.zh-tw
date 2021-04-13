---
description: IUpdateSearcher 介面會定義下列屬性。
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: IUpdateSearcher 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/11/2021
ms.locfileid: "104322583"
---
# <a name="iupdatesearcher-properties"></a>IUpdateSearcher 屬性

[**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)介面會定義下列屬性。



| 屬性                                                                                           | 描述                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | 取得和設定布林值，這個值會指出未來對 [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) 和 [**搜尋**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) 方法的呼叫是否會導致自動升級為 WINDOWS UPDATE 代理程式 (WUA) 。 |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | 識別目前的用戶端應用程式。                                                                                                                                                                                                   |
| [**IncludePotentiallySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | 取得和設定布林值，這個值會指出搜尋結果是否包含在搜尋結果中由其他更新所取代的更新。                                                                                          |
| [**線上**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | 取得和設定布林值，指出 [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) 是否上線以搜尋更新。                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | 取得和設定網站，以搜尋要搜尋的網站不是 Windows Update 網站。                                                                                                                                                         |
| [**Serverselection.sqlpolicy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | 取得和設定 [**serverselection.sqlpolicy**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) 值，指出要搜尋更新的伺服器。                                                                                                                            |




 

 

 



