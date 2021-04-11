---
title: MIDL 系結控制碼
description: 系結控制碼是代表用戶端與伺服器之間系結的資料物件。
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- 資料類型 MIDL、系結控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023308"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="a36cb-104">MIDL 系結控制碼</span><span class="sxs-lookup"><span data-stu-id="a36cb-104">MIDL Binding Handles</span></span>

<span data-ttu-id="a36cb-105">系結控制碼是代表用戶端與伺服器之間系結的資料物件。</span><span class="sxs-lookup"><span data-stu-id="a36cb-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="a36cb-106">MIDL 支援基底類型 [**控制碼 \_ t**](handle-t.md)。</span><span class="sxs-lookup"><span data-stu-id="a36cb-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="a36cb-107">這種類型的控制碼稱為「基本控制碼」。</span><span class="sxs-lookup"><span data-stu-id="a36cb-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="a36cb-108">您可以使用 **\[ handle \]** 屬性來定義您自己的控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="a36cb-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="a36cb-109">以這種方式定義的控制碼稱為「使用者定義」或「自訂」或「泛型」控制碼。</span><span class="sxs-lookup"><span data-stu-id="a36cb-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="a36cb-110">您也可以使用 **\[** [**內容 \_ 控制碼**](context-handle.md)屬性，定義維護狀態資訊的控制碼 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="a36cb-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="a36cb-111">以這種方式定義的控制碼稱為「內容」處理。</span><span class="sxs-lookup"><span data-stu-id="a36cb-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="a36cb-112">如果不需要任何狀態資訊，而且您沒有選擇呼叫 RPC 執行時間程式庫來管理控制碼，您可以要求執行時間程式庫提供自動系結。</span><span class="sxs-lookup"><span data-stu-id="a36cb-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="a36cb-113">這是藉由使用 ACF 關鍵字 **\[** [**auto \_ 控制碼**](auto-handle.md)來完成 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="a36cb-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="a36cb-114">您可以使用 ACF 關鍵字 **\[** [**隱含 \_ 控制碼**](implicit-handle.md)，將全域變數指定為系結控制碼 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="a36cb-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="a36cb-115">**\[ 明確 \_ 控制碼 \]** 關鍵字是用來指出每個遠端函式都有明確指定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a36cb-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="a36cb-116">如需詳細資訊，請參閱系結 [和控制碼](/windows/desktop/Rpc/binding-and-handles)。</span><span class="sxs-lookup"><span data-stu-id="a36cb-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 