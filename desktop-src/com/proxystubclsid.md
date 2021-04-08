---
title: ProxyStubClsid
description: 將 IID 對應至16位 proxy Dll 中的 CLSID。
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- ProxyStubClsid 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021853"
---
# <a name="proxystubclsid"></a><span data-ttu-id="80d85-104">ProxyStubClsid</span><span class="sxs-lookup"><span data-stu-id="80d85-104">ProxyStubClsid</span></span>

<span data-ttu-id="80d85-105">將 IID 對應至16位 proxy Dll 中的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="80d85-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="80d85-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="80d85-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="80d85-107">備註</span><span class="sxs-lookup"><span data-stu-id="80d85-107">Remarks</span></span>

<span data-ttu-id="80d85-108">這是指定 IID CLSID 的 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="80d85-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="80d85-109">如果您加入介面，您必須使用此專案將它們註冊 (16 位系統) ，讓 OLE 可以找到適當的遠端程式碼來建立進程間的通訊。</span><span class="sxs-lookup"><span data-stu-id="80d85-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80d85-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="80d85-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d85-111">**介面**</span><span class="sxs-lookup"><span data-stu-id="80d85-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="80d85-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="80d85-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




