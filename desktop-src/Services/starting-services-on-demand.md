---
description: 使用者可以使用 [服務] 控制台公用程式來啟動服務。 使用者可以在 [開始參數] 欄位中指定服務的引數。 服務控制程式可以啟動服務，並使用 StartService 函式指定其引數。
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: 依需求啟動服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3762721eaeaea32d42da729f57c0753b18fb951cb57ad091aa697c144df0de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888464"
---
# <a name="starting-services-on-demand"></a>依需求啟動服務

使用者可以使用 [服務] 控制台公用程式來啟動服務。 使用者可以在 [ **開始參數** ] 欄位中指定服務的引數。 服務控制程式可以啟動服務，並使用 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 函式指定其引數。

當服務啟動時，SCM 會執行下列步驟：

-   取出儲存在資料庫中的帳戶資訊。
-   登入服務帳戶。
-   載入使用者設定檔。
-   建立處於暫停狀態的服務。
-   將登入權杖指派給處理常式。
-   允許進程執行。

 

 



