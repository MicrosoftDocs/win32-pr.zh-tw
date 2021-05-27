---
title: MDM 註冊功能
description: 下列函式會在中宣告 `mdmregistration.h` ，並由 MDM 註冊使用。
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: 2ca04c3c28f3de289bad6f06feaab0aff9ef2909
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550553"
---
# <a name="mdm-registration-functions"></a>MDM 註冊功能

下列函式會在中宣告 `mdmregistration.h` ，並由 MDM 註冊使用。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**DiscoverManagementService**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | 探索 MDM 服務。 |
| [**DiscoverManagementServiceEx**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | 使用候選伺服器探索 MDM 服務。 |
| [**GetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | 取得與提供者識別碼相關聯的設定資訊。 |
| [**GetDeviceRegistrationInfo**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | 抓取裝置註冊資訊。 |
| [**GetManagementAppHyperlink**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | 抓取與 MDM 服務相關聯的管理應用程式超連結。 |
| [**IsDeviceRegisteredWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | 檢查裝置是否已向 MDM 服務註冊。 |
| [**IsManagementRegistrationAllowed**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | 檢查本機原則是否允許 MDM 註冊。 |
| [**RegisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | 使用[ \[ MS-MDE \] ：行動裝置註冊通訊協定](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)，向 MDM 服務註冊裝置。 |
| [**RegisterDeviceWithManagementUsingAADCredentials**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | 使用 Azure Active Directory (AAD) 認證，向 MDM 服務註冊裝置。 |
| [**SetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | 設定與提供者識別碼相關聯的設定資訊。 |
| [**SetManagedExternally**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | 向 MDM 代理程式指出裝置是在外部管理的，而且不會向 MDM 服務註冊。 |
| [**UnregisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | 使用 MDM 服務將裝置取消註冊。 |

## <a name="related-topics"></a>相關主題

* [MDM 註冊參考](./mdm-registration-reference.md)
