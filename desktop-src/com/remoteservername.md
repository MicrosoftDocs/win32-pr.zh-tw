---
title: RemoteServerName
description: 將用戶端設定為在呼叫未指定 COSERVERINFO 結構的啟用函式時，要求在特定電腦上執行物件。
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- RemoteServerName 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966479"
---
# <a name="remoteservername"></a>RemoteServerName

將用戶端設定為在呼叫未指定 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構的啟用函式時，要求在特定電腦上執行物件。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>備註

**RemoteServerName** 可讓用戶端應用程式進行簡單的設定管理;它們可能會在沒有硬式編碼的伺服器名稱的情況下撰寫，而且可以藉由修改所使用物件類別的 **RemoteServerName** 登錄值來進行設定。

如同 [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) 列舉和 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構的檔所述，分散式 COM 啟用的其中一個參數是 **COSERVERINFO** 結構的指標。 當這個值不是 **Null** 時， **COSERVERINFO** 結構中的資訊會覆寫函式呼叫之 **RemoteServerName** 索引鍵的設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> </dl>

 

 