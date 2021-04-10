---
title: ADSI 元件互動
description: Active Directory 路由器元件從用戶端應用程式收到第一個要求時，會從登錄中列出的已安裝 ADSI 提供者填入 ADSI 提供者資料表。
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683084"
---
# <a name="adsi-component-interaction"></a><span data-ttu-id="049d4-103">ADSI 元件互動</span><span class="sxs-lookup"><span data-stu-id="049d4-103">ADSI Component Interaction</span></span>

<span data-ttu-id="049d4-104">Active Directory 路由器元件從用戶端應用程式收到第一個要求時，會從登錄中列出的已安裝 ADSI 提供者填入 ADSI 提供者資料表。</span><span class="sxs-lookup"><span data-stu-id="049d4-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="049d4-105">如需登錄的詳細資訊，請參閱 [安裝範例提供者元件](installing-the-example-provider-component.md)。</span><span class="sxs-lookup"><span data-stu-id="049d4-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="049d4-106">從目錄對 Active Directory 物件上介面的指標提出要求的作業，是透過函式 (在 C 或 c + +) 的 Visual Basic 或 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)中的 **GetObject** ，或 ( [**IADsContainer：： GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)) 的介面方法。</span><span class="sxs-lookup"><span data-stu-id="049d4-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="049d4-107">在下圖中，ADSI 用戶端應用程式會將這類 bind 要求傳遞給 ADSI 路由器元件 (1) 。</span><span class="sxs-lookup"><span data-stu-id="049d4-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="049d4-108">路由器元件會從 ADsPath 的第一個部分識別提供者的 ProgID，並使用 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) 在登錄 (2) 中尋找相符的 CLSID，並 (3) 載入適當的提供者元件。</span><span class="sxs-lookup"><span data-stu-id="049d4-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![範例提供者中的 adsi 元件互動](images/dscspr.png)

<span data-ttu-id="049d4-110">在上圖中，提供者元件會建立代表命名目錄元素的 Active Directory 物件。</span><span class="sxs-lookup"><span data-stu-id="049d4-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="049d4-111">ADSI 支援元件會在要求的介面識別碼上進行 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="049d4-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="049d4-112">當該介面的指標被抓取 (4) 時，如同所有的 COM 用戶端/伺服器執行，系統會接著將它傳回給用戶端 (5) ，然後在用戶端應用程式上直接與提供者元件 (6) 一起運作。</span><span class="sxs-lookup"><span data-stu-id="049d4-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 