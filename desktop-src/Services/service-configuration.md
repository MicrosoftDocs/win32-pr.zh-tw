---
description: 系統會使用設定資訊來判斷如何啟動此服務。
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: 服務組態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f64b5cef835e1c7efef10c12555c81c132e707c8d1fb2814a7fcb95cf6d71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889078"
---
# <a name="service-configuration"></a>服務組態

系統會使用設定資訊來判斷如何啟動此服務。 設定資訊也包含服務顯示名稱及其描述。 例如，針對 DHCP 服務，您可以使用「動態主機設定通訊協定服務」顯示名稱，以及「為您網路上的電腦提供網際網路位址」描述。

若要修改服務物件的設定資訊，設定程式會使用 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 或 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函數。 如需範例，請參閱 [變更服務](changing-a-service-configuration.md)設定。

為了取得服務物件的設定資訊，設定程式會使用 [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) 或 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) 函數。 如需範例，請參閱 [查詢服務的](querying-a-service-s-configuration.md)設定。

[**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)和 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)服務設定函數支援使用觸發程式來控制服務啟動。

若要修改 SCManager 物件或服務物件的安全描述項，設定程式會使用 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數。 為了取得安全描述項的複本，設定程式會使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 SC 設定服務](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
