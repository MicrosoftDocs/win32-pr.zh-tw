---
title: ActivateAtStorage
description: 將用戶端設定為將相同電腦上的物件具現化，其為它們正在使用或從中初始化的持續性狀態。
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024182"
---
# <a name="activateatstorage"></a><span data-ttu-id="8cd9d-104">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="8cd9d-104">ActivateAtStorage</span></span>

<span data-ttu-id="8cd9d-105">將用戶端設定為將相同電腦上的物件具現化，其為它們正在使用或從中初始化的持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-105">Configures the client to instantiate objects on the same computer as the persistent state they are using or from which they are initialized.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8cd9d-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="8cd9d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a><span data-ttu-id="8cd9d-107">備註</span><span class="sxs-lookup"><span data-stu-id="8cd9d-107">Remarks</span></span>

<span data-ttu-id="8cd9d-108">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="8cd9d-109">開頭為 ' Y ' 或 ' y ' 的任何值都表示應使用 **ActivateAtStorage** 。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-109">Any value that begins with 'Y' or 'y' indicates that **ActivateAtStorage** should be used.</span></span>

<span data-ttu-id="8cd9d-110">**ActivateAtStorage** 功能提供透明的方式，讓用戶端能夠在與使用的資料相同的電腦上尋找執行中的物件。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-110">The **ActivateAtStorage** capability provides a transparent way to allow clients to locate running objects on the same computer as the data that they use.</span></span> <span data-ttu-id="8cd9d-111">這可減少網路流量，因為物件會執行本機檔案系統呼叫，而不是跨網路的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-111">This reduces network traffic because the object performs local file-system calls instead of calls across the network.</span></span>

<span data-ttu-id="8cd9d-112">當設定 **ActivateAtStorage** 的值時，這會成為呼叫 [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) 和 [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) 函式的預設行為，以及 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)的檔案標記實值。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-112">When a value is set for **ActivateAtStorage**, this becomes the default behavior in calls to the [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) functions, as well as to the file moniker implementation of [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="8cd9d-113">在這些呼叫中，指定 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構會覆寫函式呼叫期間的 **ActivateAtStorage** 設定。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-113">In all of these calls, specifying a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure overrides the setting of **ActivateAtStorage** for the duration of the function call.</span></span> <span data-ttu-id="8cd9d-114">呼叫端可以透過 [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)結構，將 **COSERVERINFO** 資訊傳遞至 **IMoniker：： BindToObject** 。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-114">The caller can pass **COSERVERINFO** information to **IMoniker::BindToObject** through the [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) structure.</span></span>

<span data-ttu-id="8cd9d-115"> \_ \_ 如果未在用戶端的電腦上安裝類別的登錄資訊，則在指定 CLSCTX 遠端伺服器時，ActivateAtStorage 設定的值也會是預設行為。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-115">The value set for **ActivateAtStorage** is also the default behavior when CLSCTX\_REMOTE\_SERVER is specified if no registry information for the class is installed on the client's computer.</span></span> <span data-ttu-id="8cd9d-116">為了充分利用 **ActivateAtStorage** 而撰寫的用戶端應用程式，可能需要較少的系統管理。</span><span class="sxs-lookup"><span data-stu-id="8cd9d-116">Client applications written to take advantage of **ActivateAtStorage** may therefore require less administration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cd9d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="8cd9d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd9d-118">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="8cd9d-118">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[<span data-ttu-id="8cd9d-119">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="8cd9d-119">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[<span data-ttu-id="8cd9d-120">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="8cd9d-120">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[<span data-ttu-id="8cd9d-121">**COSERVERINFO**</span><span class="sxs-lookup"><span data-stu-id="8cd9d-121">**COSERVERINFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[<span data-ttu-id="8cd9d-122">**IMoniker：： BindToObject**</span><span class="sxs-lookup"><span data-stu-id="8cd9d-122">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[<span data-ttu-id="8cd9d-123">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="8cd9d-123">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 