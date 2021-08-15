---
description: SCM 支援控制碼類型，以允許存取下列物件。
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: SCM 控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889186"
---
# <a name="scm-handles"></a>SCM 控制碼

SCM 支援控制碼類型，以允許存取下列物件。

-   已安裝服務的資料庫。
-   服務。
-   資料庫鎖定。

SCManager 物件代表已安裝服務的資料庫。 它是保存服務物件的容器物件。 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)函式會將控制碼傳回至指定電腦上的 SCManager 物件。 當您安裝、刪除、開啟和列舉服務，以及鎖定服務資料庫時，會使用這個控制碼。

服務物件代表已安裝的服務。 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)和 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)函數會傳回已安裝服務的控制碼。

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)、 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)和 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)函數可以要求不同類型的 SCManager 和服務物件存取權。 根據呼叫進程的存取權杖以及與 SCManager 或服務物件相關聯的安全描述項，授與或拒絕所要求的存取權。

[**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)函式會關閉 SCManager 和服務物件的控制碼。 當您不再需要這些控制碼時，請務必將它們關閉。

 

 



