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
# <a name="remoteservername"></a><span data-ttu-id="7d339-104">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="7d339-104">RemoteServerName</span></span>

<span data-ttu-id="7d339-105">將用戶端設定為在呼叫未指定 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構的啟用函式時，要求在特定電腦上執行物件。</span><span class="sxs-lookup"><span data-stu-id="7d339-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7d339-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="7d339-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="7d339-107">備註</span><span class="sxs-lookup"><span data-stu-id="7d339-107">Remarks</span></span>

<span data-ttu-id="7d339-108">**RemoteServerName** 可讓用戶端應用程式進行簡單的設定管理;它們可能會在沒有硬式編碼的伺服器名稱的情況下撰寫，而且可以藉由修改所使用物件類別的 **RemoteServerName** 登錄值來進行設定。</span><span class="sxs-lookup"><span data-stu-id="7d339-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="7d339-109">如同 [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) 列舉和 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構的檔所述，分散式 COM 啟用的其中一個參數是 **COSERVERINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7d339-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="7d339-110">當這個值不是 **Null** 時， **COSERVERINFO** 結構中的資訊會覆寫函式呼叫之 **RemoteServerName** 索引鍵的設定。</span><span class="sxs-lookup"><span data-stu-id="7d339-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d339-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d339-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d339-112">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="7d339-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 