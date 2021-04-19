---
description: 下列介面可以用來註冊憑證階層中的使用者或電腦。
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: 憑證註冊介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994563"
---
# <a name="certificate-enrollment-interfaces"></a>憑證註冊介面

下列介面可以用來註冊憑證階層中的使用者或電腦。



| 介面                                              | 描述                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | 註冊憑證階層中的電腦或使用者。                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | 擴充 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 介面，以從範本啟用初始化。                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | 定義可讓 web 應用程式註冊憑證、將原則伺服器認證儲存在認證快取中，以及註冊原則伺服器和註冊伺服器的方法。 |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | 捕獲憑證註冊交易的詳細錯誤資訊。                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | X.509 Simple Computer 註冊 Protocol 介面<br/>                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 




