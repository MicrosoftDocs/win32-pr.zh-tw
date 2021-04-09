---
description: 程式設計人員和系統管理員會使用服務設定程式來修改或查詢已安裝服務的資料庫。
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: 服務設定程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112781"
---
# <a name="service-configuration-programs"></a>服務設定程式

程式設計人員和系統管理員會使用服務設定程式來修改或查詢已安裝服務的資料庫。 您也可以使用登錄函數來存取資料庫。 不過，您應該只使用 SCM 設定函數，以確保已正確安裝和設定服務。

SCM 設定函數需要 SCManager 物件的控制碼或服務物件的控制碼。 若要取得這些控制碼，服務設定程式必須：

1.  您可以使用 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式來取得指定電腦上之 SCM 資料庫的控制碼。
2.  使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) 或 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數來取得服務物件的控制碼。

如需詳細資訊，請參閱下列主題：

-   [服務安裝、移除和列舉](service-installation-removal-and-enumeration.md)
-   [服務設定](service-configuration.md)
-   [使用 SC 設定服務](configuring-a-service-using-sc.md)

 

 



