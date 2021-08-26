---
title: RAS 管理 DLL 登錄設定
description: 瞭解向 RAS 註冊協力廠商遠端存取服務 (RAS) 管理 DLL 的需求。
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e40ed8fe4fe853c12e33e6168cb72cf1b3ec5b33afc92e8767731a13ec37412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036360"
---
# <a name="ras-administration-dll-registry-setup"></a>RAS 管理 DLL 登錄設定

協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

若要註冊 DLL，請在此機碼下設定下列值。



| 值名稱    | 值資料                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | **REG \_ SZ** 字串，其中包含 DLL 的使用者易記顯示名稱。 |
| *DLLPath*     | **REG \_ SZ** 字串，其中包含 DLL 的完整路徑。                  |



 

例如，名為 ProElectron，Inc. 之虛構公司的 RAS 管理 DLL 的登錄專案可能是：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* ： **REG \_ SZ** ： ProElectron RAS 管理 DLL

*DLLPath* ： **REG \_ SZ** ： C： \\ nt \\ system32 \\ntwkadm.dll

RAS 系統管理 DLL 的安裝程式也應該提供移除/卸載功能。 如果使用者移除 DLL，安裝程式應該刪除 DLL 的登錄專案。

 

 




