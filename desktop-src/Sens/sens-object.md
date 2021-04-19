---
description: 系統事件通知服務 (SENS) 將 SENS coclass 定義為 SENS 類型程式庫的一部分。
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: SENS 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975853"
---
# <a name="sens-object"></a>SENS 物件

系統事件通知服務 (SENS) 將 SENS coclass 定義為 SENS 類型程式庫的一部分。

## <a name="implementation"></a>實作

SENS 物件的執行是由作業系統提供。

## <a name="creationaccess-functions"></a>建立/存取函式



| 函式                                      | 描述                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | 使用 CLSID 來建立 SENS 物件的實例。 |



 

## <a name="interfaces"></a>介面



| 介面                            | 描述                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | 預設值。 訂閱者應用程式中接收物件所執行的輸出介面。                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | 訂閱者應用程式中接收物件所執行的輸出介面。                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | 訂閱者應用程式中接收物件所執行的輸出介面。                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | 訂閱者應用程式中接收物件所執行的輸出介面。 適用于 Windows XP。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[關於系統事件通知服務](about-system-event-notification-service.md)
</dt> </dl>

 

 
