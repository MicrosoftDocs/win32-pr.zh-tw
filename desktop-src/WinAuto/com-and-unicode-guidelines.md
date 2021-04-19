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
# <a name="com-and-unicode-guidelines"></a>COM 和 Unicode 指導方針

由於 Microsoft Active Accessibility 是以元件物件模型 (COM) 為基礎，因此開發人員需要對 COM 物件和介面進行中等程度的瞭解，而且必須知道如何執行基本工作 (例如，如何初始化 COM 程式庫) 。 伺服器開發人員必須瞭解如何設計類別來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，以及如何建立可存取的物件。

您也需要對 Unicode 有中等程度的瞭解，才能使用許多會傳回字串的 Microsoft Active Accessibility 函數。

若要有效地使用 Microsoft Active Accessibility，您應該瞭解下列 COM 和 Unicode 函數、結構、資料類型和介面。 本檔中提供了一些這些專案的有限資訊。

### <a name="functions"></a>函數：

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize)或 [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**Iunknown：： AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)和 [ **iunknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit)和 [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)和 [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)和 [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>結構和資料類型：

-   [**變異**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>COM 介面：

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>本節內容

-   [VARIANT 結構](variant-structure.md)
-   [IDispatch 介面](idispatch-interface.md)
-   [轉換 Unicode 和 ANSI 字串](converting-unicode-and-ansi-strings.md)

 

 