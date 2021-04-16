---
title: Out-Only 不接受的唯一或完整指標參數
description: MIDL 編譯器不接受僅限 \ out 的唯一或完整指標。 這類規格會導致 MIDL 編譯器產生錯誤訊息。
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508040"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="4f537-104">Out-Only 不接受的唯一或完整指標參數</span><span class="sxs-lookup"><span data-stu-id="4f537-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="4f537-105">\[ [](/windows/desktop/Midl/out-idl) \] MIDL 編譯器不接受僅限輸出的唯一或完整指標。</span><span class="sxs-lookup"><span data-stu-id="4f537-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="4f537-106">這類規格會導致 MIDL 編譯器產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4f537-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="4f537-107">自動產生的伺服器 stub 必須配置記憶體給指標引用，讓伺服器應用程式可以將資料儲存在該記憶體區域中。</span><span class="sxs-lookup"><span data-stu-id="4f537-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="4f537-108">根據 **\[ out \]** 參數的定義，系統不會將參數的相關資訊從用戶端傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="4f537-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="4f537-109">如果是唯一指標（可採用值 null），伺服器存根沒有足夠的資訊來正確複製伺服器位址空間中的唯一指標，也不會有任何資訊指出指標是否應指向有效的位址，或是否應該設定為 null。</span><span class="sxs-lookup"><span data-stu-id="4f537-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="4f537-110">因此，不允許此組合。</span><span class="sxs-lookup"><span data-stu-id="4f537-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="4f537-111">而非 \[ **out**、 [unique](/windows/desktop/Midl/unique) \] 或 \[ **out**、 [ptr](/windows/desktop/Midl/ptr) \] 指標、使用 \[ **in**、 **out**、 **unique** \] 或 \[ **in**、 **out**、 **ptr** \] 指標，或使用另一個間接取值層級，例如指向有效的 unique 或 full 指標的參考指標。</span><span class="sxs-lookup"><span data-stu-id="4f537-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 