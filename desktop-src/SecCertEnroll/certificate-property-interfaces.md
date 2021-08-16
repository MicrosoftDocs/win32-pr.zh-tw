---
description: 下列介面可以用來建立憑證屬性。
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: 憑證屬性介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3d0ab8d9f8e9bb73d47b7e112dfa0ff6fb11f70031c64405b660ee5096dd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902604"
---
# <a name="certificate-property-interfaces"></a>憑證屬性介面

下列介面可以用來建立憑證屬性。



| 介面                                                                          | 描述                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | 管理 [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) 物件的集合。                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | 將外部屬性與憑證產生關聯。                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | 表示憑證屬性，識別憑證是否已封存。                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | 代表提交給憑證授權單位單位以進行封存之加密私密金鑰的 SHA-1 雜湊。                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | 代表憑證屬性，識別已設定為啟用憑證自動註冊的範本。                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | 代表憑證屬性，識別憑證是否已備份，如果是，則為儲存的日期和時間。                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | 可讓您指定和取出包含憑證描述性資訊的字串。                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | 表示憑證屬性，此屬性包含用戶端在 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)介面上呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)方法時所建立的憑證和憑證授權單位單位資訊。 |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | 代表外部憑證屬性，其中包含 (CEP) server 的憑證註冊原則相關資訊，以及 (CES) 的憑證註冊伺服器。                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | 可讓您指定和取出包含憑證顯示名稱的字串。                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | 表示包含私密金鑰相關資訊的憑證屬性。                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | 表示憑證屬性，其中包含更新現有憑證時所建立之新憑證的 SHA-1 雜湊。                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | 代表憑證屬性，其中包含建立要求之電腦 (DNS) 名稱的網域命名系統。                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | 代表憑證屬性，其中包含建立要求之電腦 (DNS) 名稱的網域命名系統。                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 



