---
description: IAutomaticUpdatesSettings 介面會定義下列方法。
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: IAutomaticUpdatesSettings 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848605"
---
# <a name="iautomaticupdatessettings-methods"></a>IAutomaticUpdatesSettings 方法

[**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)介面會定義下列方法。



| 方法                                               | 描述                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**重新整理**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | 抓取最新的自動更新設定。 |
| [**儲存**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | 套用目前的自動更新設定。  |



 

> [!Note]  
> 在 Windows RT 上，您將無法再使用 [**IAutomaticUpdatesSettings：： Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) 方法以程式設計方式設定 Windows Update 設定。 如果您使用 [ **儲存** ] 來設定 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)) 以外的任何值，則設定作業會失敗。

 

 

 



