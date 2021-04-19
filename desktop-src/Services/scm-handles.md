---
description: SCM 支援控制碼類型，以允許存取下列物件。
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: SCM 控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975921"
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

 

 



