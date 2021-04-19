---
description: 需要適當地關閉通訊會話和整個應用程式，才能防止資源在不再需要它們的呼叫或應用程式中保持聯繫。
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: TAPI 關機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990428"
---
# <a name="tapi-shutdown"></a>TAPI 關機

需要適當地關閉通訊會話和整個應用程式，才能防止資源在不再需要它們的呼叫或應用程式中保持聯繫。

TAPI 提供一系列的功能和方法來協助處理。 很明顯地，應用程式也必須負責適當釋出配置的記憶體，不論是以資料結構或 COM 參考形式。



| TAPI 2.x 函數                                                            | Description                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | 將應用程式取消註冊為輔助電話語音通話的處理常式。 |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | 將應用程式與指定行呼叫的管理員中斷連接。  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | 關閉應用程式行抽象的使用方式。            |



 



| TAPI 3.x 介面或方法                                            | Description                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | 移除應用程式所執行的任何事件通知註冊。 |
| [**ITTAPI：： Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | 中斷應用程式與呼叫管理員的連接。                             |



 

 

 
