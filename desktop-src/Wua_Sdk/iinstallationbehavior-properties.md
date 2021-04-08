---
description: IInstallationBehavior 介面會定義下列屬性。
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: IInstallationBehavior 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943481"
---
# <a name="iinstallationbehavior-properties"></a>IInstallationBehavior 屬性

[**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)介面會定義下列屬性。



| 屬性                                                                                 | 描述                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | 取得布林值，thast 指出安裝或卸載更新是否會提示使用者輸入。                                                        |
| [**影響**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | 取得 [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) 列舉，指出更新的安裝或卸載如何影響電腦。                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | 取得 [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) 列舉，這個列舉會指定當您安裝或卸載更新時所發生的重新開機行為。 |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | 取得布林值，這個值表示安裝或卸載更新是否需要網路連接。                                                     |



 

 

 



