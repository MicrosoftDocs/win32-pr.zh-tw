---
title: 註冊 RAS 安全性 DLL
description: ras 安全性 DLL 的安裝程式必須向 Windows NT/Windows 2000 RAS 伺服器註冊 DLL。
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5ca32aa687649c80917f9a072b9d4cbeb0f1f4e8ba61ce090e7781bb04cdefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028410"
---
# <a name="registering-a-ras-security-dll"></a>註冊 RAS 安全性 DLL

ras 安全性 DLL 的安裝程式必須向 Windows NT/Windows 2000 RAS 伺服器註冊 DLL。 只有一個 RAS 安全性 DLL 可註冊為未提供多個安全性 Dll 的支援。 若要註冊 RAS 安全性 DLL，請在登錄中的下列機碼底下設定 *DLLPath* 值：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| 值名稱 | 值資料                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | **REG \_ SZ** 字串，其中包含 DLL 的路徑。 除非 DLL 位於系統路徑所列的目錄中，否則此字串應該指定完整路徑。 |



 

RAS 安全性 DLL 的安裝程式也必須提供移除/卸載功能。 如果使用者移除 DLL，安裝程式必須從登錄中刪除 *DLLPath* 值。 如果 *DLLPath* 值指定了找不到的 DLL，RAS 服務就不會啟動。

RAS 安全性 DLL 必須匯出 [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) 和 [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) 函數。

 

 




