---
title: Pointer-Attribute 類型繼承
description: 根據 DCE 規格，每個 IDL 檔案都必須定義其指標的屬性。
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382497"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="e2baa-103">Pointer-Attribute 類型繼承</span><span class="sxs-lookup"><span data-stu-id="e2baa-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="e2baa-104">根據 DCE 規格，每個 IDL 檔案都必須定義其指標的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2baa-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="e2baa-105">如果未將明確的屬性指派給指標，指標會使用 \[ [指標 \_ default](/windows/desktop/Midl/pointer-default)關鍵字所指定的值 \] 。</span><span class="sxs-lookup"><span data-stu-id="e2baa-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="e2baa-106">某些 DCE 的執行不允許未歸屬指標。</span><span class="sxs-lookup"><span data-stu-id="e2baa-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="e2baa-107">如果指標沒有明確的屬性，IDL 檔案必須具有 **\[ 指標 \_ 預設 \]** 規格，才能設定指標屬性。</span><span class="sxs-lookup"><span data-stu-id="e2baa-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="e2baa-108">在預設的 (Microsoft 擴充功能) 模式中，您可以在匯入定義 IDL 檔案的 IDL 檔案中指定指標的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2baa-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="e2baa-109">在一個 IDL 檔中定義的指標，可以繼承其他 IDL 檔案中指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2baa-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="e2baa-110">此外，在預設模式下，IDL 檔案可以包含未歸屬指標。</span><span class="sxs-lookup"><span data-stu-id="e2baa-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="e2baa-111">如果基底和匯入的 IDL 檔案都沒有指定指標屬性或 **\[ 指標 \_ 預設值 \]**，則會將未歸屬指標解釋為唯一指標。</span><span class="sxs-lookup"><span data-stu-id="e2baa-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="e2baa-112">MIDL 編譯器會使用下列優先順序規則，將指標屬性指派給指標 (1 為最高) 。</span><span class="sxs-lookup"><span data-stu-id="e2baa-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="e2baa-113">優先順序</span><span class="sxs-lookup"><span data-stu-id="e2baa-113">Priority</span></span> | <span data-ttu-id="e2baa-114">描述</span><span class="sxs-lookup"><span data-stu-id="e2baa-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2baa-115">1</span><span class="sxs-lookup"><span data-stu-id="e2baa-115">1</span></span>        | <span data-ttu-id="e2baa-116">明確指標屬性會套用至定義或使用網站上的指標。</span><span class="sxs-lookup"><span data-stu-id="e2baa-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="e2baa-117">2</span><span class="sxs-lookup"><span data-stu-id="e2baa-117">2</span></span>        | <span data-ttu-id="e2baa-118">預設值是 IDL 檔案中定義型別的 **\[ 指標 \_ default \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2baa-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="e2baa-119">3</span><span class="sxs-lookup"><span data-stu-id="e2baa-119">3</span></span>        | <span data-ttu-id="e2baa-120">預設值是匯入類型之 IDL 檔案中的 **\[ 指標 \_ 預設 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2baa-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="e2baa-121">4</span><span class="sxs-lookup"><span data-stu-id="e2baa-121">4</span></span>        | <span data-ttu-id="e2baa-122">預設值是 \[ [](/windows/desktop/Midl/ptr) \] DCE 相容性模式中的 Ptr，或 \[ [](/windows/desktop/Midl/unique) \] 在 Microsoft 擴充模式中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e2baa-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 