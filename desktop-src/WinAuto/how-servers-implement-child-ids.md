---
title: 伺服器如何執行子系識別碼
description: 伺服器開發人員可以將子識別碼指派給簡單的元素和可存取的物件。 不過，建議的方法是在每個具有子系的可存取物件中，支援標準元件物件模型 (COM) 介面 IEnumVARIANT。
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933411"
---
# <a name="how-servers-implement-child-ids"></a><span data-ttu-id="fde1b-104">伺服器如何執行子系識別碼</span><span class="sxs-lookup"><span data-stu-id="fde1b-104">How Servers Implement Child IDs</span></span>

<span data-ttu-id="fde1b-105">伺服器開發人員可以將子識別碼指派給簡單的元素和可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="fde1b-105">Server developers can assign child IDs to both simple elements and accessible objects.</span></span> <span data-ttu-id="fde1b-106">不過，建議的方法是在每個具有子系的可存取物件中，支援標準元件物件模型 (COM) 介面 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 。</span><span class="sxs-lookup"><span data-stu-id="fde1b-106">However, the recommended approach is to support the standard Component Object Model (COM) interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in every accessible object that has children.</span></span>

<span data-ttu-id="fde1b-107">如果您執行 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)，則必須：</span><span class="sxs-lookup"><span data-stu-id="fde1b-107">If you implement [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must:</span></span>

-   <span data-ttu-id="fde1b-108">列舉所有子系，簡單元素和可存取的物件都是。</span><span class="sxs-lookup"><span data-stu-id="fde1b-108">Enumerate all children, both simple elements and accessible objects.</span></span> <span data-ttu-id="fde1b-109">為所有簡單的專案提供子系識別碼，並將 [**IDispatch**](idispatch-interface.md) 提供給每個可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="fde1b-109">Provide child IDs for all simple elements and provide the [**IDispatch**](idispatch-interface.md) to each accessible object.</span></span>
-   <span data-ttu-id="fde1b-110">針對可存取的物件，將 [**VARIANT**](variant-structure.md)的 **vt** 成員設定為 vt \_ 分派。</span><span class="sxs-lookup"><span data-stu-id="fde1b-110">For accessible objects, set the **vt** member of the [**VARIANT**](variant-structure.md) to VT\_DISPATCH.</span></span> <span data-ttu-id="fde1b-111">**PdispVal** 成員必須包含 [**IDispatch**](idispatch-interface.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fde1b-111">The **pdispVal** member must contain a pointer to the [**IDispatch**](idispatch-interface.md) interface.</span></span> <span data-ttu-id="fde1b-112">請注意， **變數** 會由用戶端配置及釋放。</span><span class="sxs-lookup"><span data-stu-id="fde1b-112">Note that the **VARIANT** is allocated and freed by the client.</span></span>
-   <span data-ttu-id="fde1b-113">針對簡單的專案，子系識別碼為任何32位正整數。</span><span class="sxs-lookup"><span data-stu-id="fde1b-113">For simple elements, the child ID is any 32-bit positive integer.</span></span> <span data-ttu-id="fde1b-114">請注意，Microsoft Active Accessibility 會保留零和負整數。</span><span class="sxs-lookup"><span data-stu-id="fde1b-114">Note that zero and negative integers are reserved by Microsoft Active Accessibility.</span></span> <span data-ttu-id="fde1b-115">將 [**VARIANT**](variant-structure.md) 結構 **vt** 成員設定為 vt \_ I4，並將 **LVAL** 成員設定為子系識別碼。</span><span class="sxs-lookup"><span data-stu-id="fde1b-115">Set the [**VARIANT**](variant-structure.md) structure **vt** member to VT\_I4 and the **lVal** member to the child ID.</span></span>

<span data-ttu-id="fde1b-116">如果您不支援 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)，則必須在每個物件中，依序從1開始指派子系識別碼和子系的編號。</span><span class="sxs-lookup"><span data-stu-id="fde1b-116">If you do not support [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must assign child IDs and number the children in each object sequentially starting with one.</span></span>

<span data-ttu-id="fde1b-117">建議用戶端使用 Microsoft Active Accessibility 函數 [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) ，而不是直接呼叫伺服器 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="fde1b-117">It is recommended that clients use the Microsoft Active Accessibility function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) rather than call the server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface directly.</span></span>

 

 