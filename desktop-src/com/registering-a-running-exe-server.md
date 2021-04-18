---
title: 註冊正在執行的 EXE 伺服器
description: 註冊正在執行的 EXE 伺服器
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301671"
---
# <a name="registering-a-running-exe-server"></a>註冊正在執行的 EXE 伺服器

啟動可執行檔 (EXE) server 時，它應該呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)，它會在與執行中的物件資料表) 不同的資料表 (不同的資料表中，註冊伺服器的 CLSID。 當伺服器在類別資料表中註冊時，它會允許服務控制管理員 (SCM) 判斷不需要重新開機類別，因為伺服器已經在執行中。 只有在伺服器未列于類別表中時，SCM 才能檢查登錄是否有適當的值，並啟動與指定 CLSID 相關聯的伺服器。

您會將類別的 CLSID 和其 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面的指標傳遞給 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) 。 後續使用此 CLSID 來呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 的用戶端，將會取得其所要求介面的指標，只要安全性不會禁止它即可。  (請參閱 [實例建立](instance-creation-helper-functions.md) 協助程式函數，以取得數個實例建立和啟用函式的描述。 ) 

當下列所有條件都成立時，類別物件的伺服器應該呼叫 [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) 來撤銷類別物件 (移除其註冊) ：

-   沒有物件定義的現有實例。
-   類別物件上沒有鎖定。
-   提供服務給類別物件的應用程式不在使用者控制項下， (顯示) 的使用者看不到。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安裝為服務應用程式](installing-as-a-service-application.md)
</dt> <dt>

[在安裝時註冊類別](registering-a-class-at-installation.md)
</dt> <dt>

[在 ROT 中註冊物件](registering-objects-in-the-rot.md)
</dt> <dt>

[自我註冊](self-registration.md)
</dt> </dl>

 

 




