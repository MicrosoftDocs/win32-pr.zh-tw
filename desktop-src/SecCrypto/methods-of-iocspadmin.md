---
description: 下列方法是由 IOCSPAdmin 介面所定義。 這裡不會顯示內容存取方法。 若要查看 IOCSPAdmin 的屬性，請參閱 IOCSPAdmin 的屬性。
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: IOCSPAdmin 的方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318515"
---
# <a name="methods-of-iocspadmin"></a>IOCSPAdmin 的方法

下列方法是由 [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) 介面所定義。 這裡不會顯示內容存取方法。 若要查看 **IOCSPAdmin** 的屬性，請參閱 [IOCSPAdmin 的屬性](properties-of-iocspadmin.md)。



| 方法                                                              | 描述                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | 連接至線上憑證狀態通訊協定 (OCSP) 回應程式伺服器，並使用伺服器的設定資訊來初始化 **OCSPAdmin** 物件。                                                                                                     |
| [**GetHashAlgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | 取得雜湊演算法名稱的清單。 回應者伺服器會使用其中一個已命名的演算法，來為指定的 [*憑證授權單位*](../secgloss/c-gly.md) 單位簽署 OCSP 回應 (CA) 設定。 |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | 取得指定回應者伺服器上使用者的許可權角色存取遮罩。                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | 取得回應者伺服器的安全描述項資訊。                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | 取得指定 CA 憑證的回應者伺服器上可用的簽署憑證。                                                                                                                                                                        |
| [**坪**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | 測試與回應者服務的 DCOM 連接。                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | 更新具有設定變更的回應者服務。                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | 更新 OCSP 回應程式伺服器的安全描述項資訊。                                                                                                                                                                                                     |



 

 

 
