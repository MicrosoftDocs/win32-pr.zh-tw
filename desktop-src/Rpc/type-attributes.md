---
title: 類型屬性
description: 遠端程序呼叫 (RPC) ，以及可套用至型別宣告的 MIDL 型別屬性。
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842320"
---
# <a name="type-attributes"></a><span data-ttu-id="be4c1-103">類型屬性</span><span class="sxs-lookup"><span data-stu-id="be4c1-103">Type Attributes</span></span>

<span data-ttu-id="be4c1-104">型別屬性是可套用至型別宣告的 MIDL 屬性：</span><span class="sxs-lookup"><span data-stu-id="be4c1-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="be4c1-105">**\[**[**處理**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="be4c1-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="be4c1-106">**\[**[**內容 \_ 控制碼**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="be4c1-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="be4c1-107">**\[**[**切換 \_ 類型**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="be4c1-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="be4c1-108">指標類型屬性</span><span class="sxs-lookup"><span data-stu-id="be4c1-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="be4c1-109">**\[ Switch \_ type \]** 屬性會指定聯集鑒別子的類型。</span><span class="sxs-lookup"><span data-stu-id="be4c1-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="be4c1-110">這個屬性只適用于 nonencapsulated 聯集。</span><span class="sxs-lookup"><span data-stu-id="be4c1-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="be4c1-111">內容控制碼是具有 **\[ 內容 \_ 控制碼 \]** 屬性的指標。</span><span class="sxs-lookup"><span data-stu-id="be4c1-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="be4c1-112">**\[ 內容 \_ 控制碼 \]** 屬性可讓您撰寫程式，以便在遠端程序呼叫之間維護狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="be4c1-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="be4c1-113">具有非 null 值的內容控制碼代表儲存的內容，而且有兩個用途：</span><span class="sxs-lookup"><span data-stu-id="be4c1-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="be4c1-114">在用戶端上，它包含 RPC 執行時間程式庫將呼叫導向伺服器所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="be4c1-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="be4c1-115">在伺服器端，它會作為作用中內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="be4c1-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="be4c1-116">**\[** [**Handle**](/windows/desktop/Midl/handle) **\]** 屬性指定型別可以做為使用者定義的 (泛型) 控制碼來進行。</span><span class="sxs-lookup"><span data-stu-id="be4c1-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="be4c1-117">這項功能允許設計對應用程式有意義的控制碼。</span><span class="sxs-lookup"><span data-stu-id="be4c1-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="be4c1-118">使用者必須提供系結和解除系結常式，才能在使用者定義的控制碼類型與 RPC 基本控制碼類型之間轉換， **處理 \_ t**。</span><span class="sxs-lookup"><span data-stu-id="be4c1-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="be4c1-119">基本控制碼包含對 RPC 執行時間程式庫有意義的目的地資訊。</span><span class="sxs-lookup"><span data-stu-id="be4c1-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="be4c1-120">使用者定義控制碼只能在類型宣告中定義，而不能定義在函式宣告中。</span><span class="sxs-lookup"><span data-stu-id="be4c1-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="be4c1-121">具有 **\[ handle \]** 屬性的參數具有雙重用途。</span><span class="sxs-lookup"><span data-stu-id="be4c1-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="be4c1-122">它是用來判斷呼叫的系結，而且會以一般資料參數的形式傳送至呼叫的程式。</span><span class="sxs-lookup"><span data-stu-id="be4c1-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 