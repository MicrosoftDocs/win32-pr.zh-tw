---
title: 關於 RAS 管理 DLL 登錄設定
description: 瞭解向 RAS 註冊協力廠商遠端存取服務 (RAS) 管理 DLL 的需求。 RAS 支援多個 RAS 管理 Dll。
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS 管理 RRAS，DLL 登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dbabc7a667455bce2cffbd3d04591076f820efa755c0f512f27130a82fde4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909908"
---
# <a name="about-ras-administration-dll-registry-setup"></a>關於 RAS 管理 DLL 登錄設定

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



 

由於 RAS 支援多個 RAS 管理 Dll，因此登錄值 **DLLPath** 可以包含以分號分隔的路徑清單。 例如，名為 ProElectron，Inc. 之虛構公司的 RAS 管理 DLL 的登錄專案可能如下所示：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*： **REG \_ SZ** ： ProElectron RAS 管理 DLL

*DLLPath*： **REG \_ SZ** ： C： \\ nt \\ system32 \\ntwkadm.dll;C： \\ nt \\ system32 \\ntwkadm2.dll

RAS 會依此登錄值列出 Dll 的順序來呼叫它們。 登錄值 *DisplayName* 仍只包含單一顯示名稱。

RAS 系統管理 DLL 的安裝程式也必須提供移除和卸載功能。 如果使用者移除 DLL，安裝程式必須刪除 DLL 的登錄專案。

**Windows 2000/NT：** RAS 只支援一個 RAS 管理 DLL，因此登錄值 **DLLPath** 不能包含以分號分隔的路徑清單。

 

 




