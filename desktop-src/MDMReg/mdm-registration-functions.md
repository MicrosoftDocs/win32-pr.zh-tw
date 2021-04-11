---
title: MDM 註冊功能
description: MDM 註冊會使用下列功能。
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316609"
---
# <a name="mdm-registration-functions"></a>MDM 註冊功能

MDM 註冊會使用下列功能。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**DiscoverManagementService**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

探索 MDM 服務。

</dd> <dt>

[**DiscoverManagementServiceEx**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

使用候選伺服器探索 MDM 服務。

</dd> <dt>

[**GetDeviceRegistrationInfo**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

抓取裝置註冊資訊。

</dd> <dt>

[**GetManagementAppHyperlink**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

抓取與 MDM 服務相關聯的管理應用程式超連結。

</dd> <dt>

[**IsDeviceRegisteredWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

檢查裝置是否已向 MDM 服務註冊。

</dd> <dt>

[**IsManagementRegistrationAllowed**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

檢查本機原則是否允許 MDM 註冊。

</dd> <dt>

[**RegisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

使用[ \[ MS-MDE \] ：行動裝置註冊通訊協定](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)，向 MDM 服務註冊裝置。

</dd> <dt>

[**RegisterDeviceWithManagementUsingAADCredentials**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

使用 Azure Active Directory (AAD) 認證，向 MDM 服務註冊裝置。

</dd> <dt>

[**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

向 MDM 代理程式指出裝置是在外部管理的，而且不會向 MDM 服務註冊。

</dd> <dt>

[**UnregisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

使用 MDM 服務取消註冊裝置

</dd> </dl>

 

 