---
description: 智慧卡驗證
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: 智慧卡驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985032"
---
# <a name="smart-card-authentication"></a>智慧卡驗證

[*智慧卡子系統*](../secgloss/s-gly.md)的基本部分是根據 PC/SC 標準 (請參閱) 的規格 [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) 。 這些基本元件包括：

-   使用 Windows API 的 [*資源管理員*](../secgloss/r-gly.md) 。
-   可搭配資源管理員使用的 [*使用者介面*](../secgloss/u-gly.md) (UI) 。
-   提供特定服務存取權的數個基底 [*服務提供者*](../secgloss/s-gly.md) 。 相對於 resource manager 的 Windows API，服務提供者會使用 COM 介面模型來提供 [*智慧卡*](../secgloss/s-gly.md) 服務。

下圖顯示這些元件在整體智慧卡架構中的關聯性。

![智慧卡架構](images/smartovr2a.png)

如需 [*智慧卡子系統*](../secgloss/s-gly.md) 如何與 Microsoft Internet Security Framework 中提供的其他服務搭配運作的詳細資訊，請參閱與 [其他服務相關](relation-to-other-services.md)的資訊。

如需智慧卡驗證的相關資訊，請參閱下列主題。



| 主題                                                                      | 目錄                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [智慧卡概念](smart-card-concepts.md)<br/>                   | 使用者與智慧卡之間互動的基本概念和描述。<br/>                                                                                                                                                        |
| [智慧卡 Resource Manager](smart-card-resource-manager.md)<br/>   | 資源管理員 API 的相關資訊，可管理 [*讀取器*](../secgloss/r-gly.md) 和 [*智慧卡*](../secgloss/s-gly.md)的存取權。<br/> |
| [智慧卡消費者介面](smart-card-user-interface.md)<br/>       | [ [*智慧卡一般] 對話方塊*](../secgloss/s-gly.md)的相關資訊。<br/>                                                                                   |
| [智慧卡服務提供者](smart-card-service-providers.md)<br/> | 提供智慧卡功能之介面、命令和包裝函式的相關資訊。<br/>                                                                                                                                              |



 

此外，您可以在中找到目前的 Microsoft 智慧卡開發 [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) 。

 

 
