---
description: WMI 服務管理類別是用來管理 WMI 服務本身，而不是電腦系統或商業網路。 管理 WMI 包含設定 WMI 服務和管理 WMI 作業。
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: WMI 服務管理類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 879044411a0bcba63900de648c798863e764261fe80934bbc914a01854ae8f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079512"
---
# <a name="wmi-service-management-classes"></a>WMI 服務管理類別

WMI 服務管理類別是用來管理 WMI 服務本身，而不是電腦系統或商業網路。 管理 WMI 包含設定 WMI 服務和管理 WMI 作業。

WMI 服務管理類別包含下列類別的子類別：

-   [WMI 設定類別](#wmi-configuration-classes)
-   [WMI 管理類別](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a>WMI 設定類別

WMI 設定類別會衍生設定 WMI 服務的方法。

以下是 WMI 設定類別的表格。



| 類別                                                             | 描述                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md) | 抽象的基類，這個基類會實作為衍生自這個類別的方法參數。 |



 

## <a name="wmi-management-classes"></a>WMI 管理類別

WMI 管理類別代表 WMI 服務的指令引數。

以下是 WMI 管理類別的表格。



| 類別                                                       | 描述                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Win32 \_ WMISetting**](win32-wmisetting.md)               | 包含 WMI 服務的指令引數。                                      |
| [**Win32 \_ WMIElementSetting**](win32-wmielementsetting.md) | 在 Windows 系統中執行的服務與其可使用的 WMI 設定之間的關聯。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Win32 類別](./win32-provider.md)
</dt> </dl>

 

 
