---
description: IUpdateServiceRegistration 介面會定義下列屬性。
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: IUpdateServiceRegistration 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973415"
---
# <a name="iupdateserviceregistration-properties"></a>IUpdateServiceRegistration 屬性

**IUpdateServiceRegistration** 介面會定義下列屬性。



| 屬性                                                                                      | 描述                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPendingRegistrationWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | 取得布林值，這個值會指出服務是否也會在新增時向自動更新註冊。                                  |
| [**>registrationstate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | 取得 [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) 值，這個值表示服務註冊的目前狀態。 |
| [**服務**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | 取得 [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) 介面的指標。 這個屬性是預設屬性。                                    |



 

 

 



