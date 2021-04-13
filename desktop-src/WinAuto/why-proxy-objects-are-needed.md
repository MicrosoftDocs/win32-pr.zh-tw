---
title: 為何需要 Proxy 物件
description: 使用可存取的物件時，當用戶端設定同內容攔截函式時，會將執行用戶端攔截函式的 DLL 載入伺服器的位址空間中。
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300836"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="d9167-103">為何需要 Proxy 物件</span><span class="sxs-lookup"><span data-stu-id="d9167-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="d9167-104">使用可存取的物件時，當用戶端設定同內容攔截函 [式](in-context-and-out-of-context-hook-functions.md)時，會將執行用戶端攔截函式的 DLL 載入伺服器的位址空間中。</span><span class="sxs-lookup"><span data-stu-id="d9167-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="d9167-105">在此情況下，當用戶端從攔截函式內呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 時，傳回的介面指標會直接指向伺服器位址空間中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d9167-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="d9167-106">當用戶端使用這個指標呼叫介面屬性時，元件物件模型 (COM) 程式庫不涉及封送處理或封送處理，而且無法偵測是否終結物件。</span><span class="sxs-lookup"><span data-stu-id="d9167-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="d9167-107">因此，伺服器必須偵測到這種情況，並將錯誤碼傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="d9167-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




