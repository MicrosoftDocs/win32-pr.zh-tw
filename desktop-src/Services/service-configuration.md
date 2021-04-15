---
description: 系統會使用設定資訊來判斷如何啟動此服務。
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: 服務組態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511209"
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

 

 
