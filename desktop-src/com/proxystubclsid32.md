---
title: ProxyStubClsid32
description: 將 IID 對應至32位 proxy Dll 中的 CLSID。
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316555"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="af2b9-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="af2b9-104">ProxyStubClsid32</span></span>

<span data-ttu-id="af2b9-105">將 IID 對應至32位 proxy Dll 中的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="af2b9-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="af2b9-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="af2b9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="af2b9-107">備註</span><span class="sxs-lookup"><span data-stu-id="af2b9-107">Remarks</span></span>

<span data-ttu-id="af2b9-108">這是指定 IID CLSID 的 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="af2b9-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="af2b9-109">這是必要的專案，因為在16位和32位介面上，IID 對 CLSID 的對應可能會不同。</span><span class="sxs-lookup"><span data-stu-id="af2b9-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="af2b9-110">IID 對 CLSID 的對應取決於將介面 proxy 封裝成一組 proxy Dll 的方式。</span><span class="sxs-lookup"><span data-stu-id="af2b9-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="af2b9-111">如果您加入介面，您必須使用此專案將它們註冊 (32 位系統) ，讓 OLE 可以找到適當的遠端程式碼來建立進程間的通訊。</span><span class="sxs-lookup"><span data-stu-id="af2b9-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af2b9-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="af2b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2b9-113">**IMarshal**</span><span class="sxs-lookup"><span data-stu-id="af2b9-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="af2b9-114">**介面**</span><span class="sxs-lookup"><span data-stu-id="af2b9-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="af2b9-115">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="af2b9-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 