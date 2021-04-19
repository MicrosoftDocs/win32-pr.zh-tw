---
title: COM 和 Unicode 指導方針
description: 由於 Microsoft Active Accessibility 是以元件物件模型 (COM) 為基礎，因此開發人員需要對 COM 物件和介面進行中等程度的瞭解，而且必須知道如何執行基本工作 (例如，如何初始化 COM 程式庫) 。
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001281"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="e7bcd-103">COM 和 Unicode 指導方針</span><span class="sxs-lookup"><span data-stu-id="e7bcd-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="e7bcd-104">由於 Microsoft Active Accessibility 是以元件物件模型 (COM) 為基礎，因此開發人員需要對 COM 物件和介面進行中等程度的瞭解，而且必須知道如何執行基本工作 (例如，如何初始化 COM 程式庫) 。</span><span class="sxs-lookup"><span data-stu-id="e7bcd-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="e7bcd-105">伺服器開發人員必須瞭解如何設計類別來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，以及如何建立可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="e7bcd-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="e7bcd-106">您也需要對 Unicode 有中等程度的瞭解，才能使用許多會傳回字串的 Microsoft Active Accessibility 函數。</span><span class="sxs-lookup"><span data-stu-id="e7bcd-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="e7bcd-107">若要有效地使用 Microsoft Active Accessibility，您應該瞭解下列 COM 和 Unicode 函數、結構、資料類型和介面。</span><span class="sxs-lookup"><span data-stu-id="e7bcd-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="e7bcd-108">本檔中提供了一些這些專案的有限資訊。</span><span class="sxs-lookup"><span data-stu-id="e7bcd-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="e7bcd-109">函數：</span><span class="sxs-lookup"><span data-stu-id="e7bcd-109">Functions:</span></span>

-   [<span data-ttu-id="e7bcd-110">**OleInitialize**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="e7bcd-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize)或 [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="e7bcd-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="e7bcd-112">[**Iunknown：： AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)和 [ **iunknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="e7bcd-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="e7bcd-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit)和 [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="e7bcd-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="e7bcd-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)和 [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="e7bcd-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="e7bcd-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)和 [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="e7bcd-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="e7bcd-116">結構和資料類型：</span><span class="sxs-lookup"><span data-stu-id="e7bcd-116">Structures and data types:</span></span>

-   [<span data-ttu-id="e7bcd-117">**變異**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="e7bcd-118">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="e7bcd-119">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="e7bcd-120">COM 介面：</span><span class="sxs-lookup"><span data-stu-id="e7bcd-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="e7bcd-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="e7bcd-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="e7bcd-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="e7bcd-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="e7bcd-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="e7bcd-124">In this section</span></span>

-   [<span data-ttu-id="e7bcd-125">VARIANT 結構</span><span class="sxs-lookup"><span data-stu-id="e7bcd-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="e7bcd-126">IDispatch 介面</span><span class="sxs-lookup"><span data-stu-id="e7bcd-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="e7bcd-127">轉換 Unicode 和 ANSI 字串</span><span class="sxs-lookup"><span data-stu-id="e7bcd-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 