---
title: 尋找遠端物件
description: 尋找遠端物件
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842807"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="f3b06-103">尋找遠端物件</span><span class="sxs-lookup"><span data-stu-id="f3b06-103">Locating a Remote Object</span></span>

<span data-ttu-id="f3b06-104">隨著分散式系統的 COM 的出現，COM 會針對 [Com 類別物件和 clsid](com-class-objects-and-clsids.md) 中所述的物件建立使用基本模型，並新增一個以上的方法來找出可能位於網路中另一個系統上的物件，而不需要造成用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="f3b06-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="f3b06-105">COM 已新增登錄機碼，以允許伺服器登錄所在的電腦名稱稱，或現有存放裝置所在的電腦。</span><span class="sxs-lookup"><span data-stu-id="f3b06-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="f3b06-106">因此，用戶端應用程式只需要知道伺服器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="f3b06-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="f3b06-107">不過，在需要的情況下，COM 已將 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 的先前保留參數取代為 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構，此結構可讓用戶端指定伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="f3b06-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="f3b06-108">**CoGetClassObject** 函式中的另一個重要值是 [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)列舉，這個列舉會指定預期的物件是在同進程、跨進程的本機或跨進程的遠端執行。</span><span class="sxs-lookup"><span data-stu-id="f3b06-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="f3b06-109">結合這兩個值和登錄中的值，可決定要執行物件的方式和位置。</span><span class="sxs-lookup"><span data-stu-id="f3b06-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="f3b06-110">實例建立呼叫會在指定伺服器位置時，覆寫登錄設定。</span><span class="sxs-lookup"><span data-stu-id="f3b06-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="f3b06-111">COM 用來執行這項操作的演算法，在 [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) 列舉的參考中有所說明。</span><span class="sxs-lookup"><span data-stu-id="f3b06-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="f3b06-112">遠端啟用取決於用戶端與伺服器之間的安全性關聯性。</span><span class="sxs-lookup"><span data-stu-id="f3b06-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="f3b06-113">如需詳細資訊，請參閱 [COM 中的安全性](security-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="f3b06-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3b06-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3b06-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b06-115">COM 類別物件和 Clsid</span><span class="sxs-lookup"><span data-stu-id="f3b06-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="f3b06-116">透過類別物件建立物件</span><span class="sxs-lookup"><span data-stu-id="f3b06-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 