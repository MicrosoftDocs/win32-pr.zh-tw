---
title: 屬性集序列化
description: 屬性集序列化格式有兩個版本。
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c635728e169cdddb20437323a49a18496b3459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186022"
---
# <a name="property-set-serialization"></a>屬性集序列化

屬性集序列化格式有兩個版本。 原始規格描述版本0的格式。 如需詳細資訊，請參閱 [格式版本](format-version.md) 。 第1版延伸原始版本。 所有版本0屬性集都是有效的第1版屬性集。 序列化屬性集標頭中的 [ **格式版本** ] 欄位表示版本。

下列專案會識別 version 0 和第1版屬性集序列化格式之間的差異。

-   支援新的 **VARTYPE** 值。 如需 **VARTYPE** 值和其使用方式的詳細資訊，請參閱 [IDispatch 資料類型和結構]( /previous-versions/ms221600(v=vs.100)) 和 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構主題。

    版本0屬性集不支援下列 **VARTYPE** 值，但在第1版中支援：

    VT \_ I1

    VT \_ 向量 \| vt \_ I1

    VT \_ INT

    VT \_ UINT

    VT \_ DECIMAL

    此外，Safearray 也可以在屬性集內進行序列化。 SafeArray 的出現是由 \_ 使用 **OR** 運算的 vt 陣列位所表示，並搭配 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **VT** 成員中的陣列元素。 例如，4位元組帶正負號整數的 SafeArray 有一種 VT \_ 陣列 \| vt \_ I4。

    下列元素類型對序列化屬性集中的 SafeArray 有效：



|             |          |             |           |
|-------------|----------|-------------|-----------|
| VT \_ I1      | VT \_ UI1  | VT \_ I2      | VT \_ UI2   |
| VT \_ I4      | VT \_ UI4  | VT \_ INT     | VT \_ UINT  |
| VT \_ R4      | VT \_ R8   | VT \_ CY      | VT \_ 日期  |
| VT \_ BSTR    | VT \_ BOOL | VT \_ DECIMAL | VT \_ 錯誤 |
| VT \_ 變異 |          |             |           |



 

\_指定 VT VARIANT 資料類型時，它會指出 SafeArray 本身會保存 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構。 這些元素的類型必須來自于上述清單，但它們不能包含嵌套的 VT \_ 變異類型。

請注意， [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的執行必須能夠在遇到新類型時傳回錯誤，以順利復原。例如，VARENUM 類型。

-   區分大小寫的屬性名稱。 屬性名稱（例如，在 [**IPropertyStorage：： WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) 方法中指定的名稱）在版本0屬性集中不區分大小寫。 在第1版的屬性集中，屬性名稱可能會區分大小寫，端視新的行為屬性的值而定。

    行為屬性是具有 VT UI4 類型的 [屬性識別碼 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) \_ 。 如果設定此值的最小位，屬性集名稱會區分大小寫。 \_ \_ 在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)方法的 *grfFlags* 參數中，設定區分大小寫的 PROPSETFLAG 旗標，以指定區分大小寫的屬性集。

-   長屬性名稱。 版本0屬性集的屬性名稱必須小於或等於256個字元，包括字串結束字元（適用于 Unicode 字碼頁中的屬性集）。 如果不在 Unicode 字碼頁中，則必須小於256個位元組。 另一方面，第1版屬性集會擁有無限制長度的屬性名稱，不過它們仍受限於 256 kb 的整體屬性集大小限制 (KB) 。

建議 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的執行預設會建立和維護第0版的屬性集。 如果呼叫端隨後要求第1版格式的特定功能，則只應該更新屬性集的版本。 例如，如果撰寫型別 VT 陣列的屬性 \_ ，或寫入 long 屬性名稱，則實作為應將屬性集格式更新為第1版。 如果在 \_ \_ [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的呼叫中指定 PROPSETFLAG 區分大小寫的列舉值，就會發生這個指導方針的例外狀況。 在此情況下，必須將屬性集建立為第1版屬性集。

 

 