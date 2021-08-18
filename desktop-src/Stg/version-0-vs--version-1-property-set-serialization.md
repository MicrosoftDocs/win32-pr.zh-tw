---
title: 屬性集序列化
description: 屬性集序列化格式有兩個版本。
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9412fd2a83ab7c71b97888d4ae7911a96fdc4cfe5a9ebbceb5d985b3a5e2b418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886473"
---
# <a name="property-set-serialization"></a>屬性集序列化

屬性集序列化格式有兩個版本。 原始規格描述版本0的格式。 如需詳細資訊，請參閱 [格式版本](format-version.md) 。 第1版延伸原始版本。 所有版本0屬性集都是有效的第1版屬性集。 序列化屬性集標頭中的 [ **格式版本** ] 欄位表示版本。

下列專案會識別 version 0 和第1版屬性集序列化格式之間的差異。

-   支援新的 **VARTYPE** 值。 如需 **VARTYPE** 值和其使用方式的詳細資訊，請參閱 [IDispatch 資料類型和結構]( /previous-versions/ms221600(v=vs.100)) 和 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構主題。

    版本0屬性集不支援下列 **VARTYPE** 值，但在第1版中支援：

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    此外，Safearray 也可以在屬性集內進行序列化。 如果有 SafeArray，則會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)結構的 **VT** 成員中的陣列元素組合，使用 **OR** 運算 VT_ARRAY 來表示 SafeArray 的存在。 例如，4位元組帶正負號整數的 SafeArray 具有類型的 VT_ARRAY \| VT_I4。

    下列元素類型對序列化屬性集中的 SafeArray 有效：

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    當指定 VT_VARIANT 資料類型時，它會指出 SafeArray 本身會保存 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。 這些元素的類型必須來自于上述清單，但它們不能包含嵌套 VT_VARIANT 類型。
    
    請注意， [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的執行必須能夠在遇到新類型時傳回錯誤，以順利復原。例如，VARENUM 類型。

-   區分大小寫的屬性名稱。 屬性名稱（例如，在 [**IPropertyStorage：： WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) 方法中指定的名稱）在版本0屬性集中不區分大小寫。 在第1版的屬性集中，屬性名稱可能會區分大小寫，端視新的行為屬性的值而定。

    行為屬性是類型為 VT_UI4 的 [屬性識別碼 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) 。 如果設定此值的最小位，屬性集名稱會區分大小寫。 在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)方法的 *grfFlags* 參數中設定 PROPSETFLAG_CASE_SENSITIVE 旗標，以指定區分大小寫的屬性集。

-   長屬性名稱。 版本0屬性集的屬性名稱必須小於或等於256個字元，包括字串結束字元（適用于 Unicode 字碼頁中的屬性集）。 如果不在 Unicode 字碼頁中，則必須小於256個位元組。 另一方面，第1版屬性集會擁有無限制長度的屬性名稱，不過它們仍受限於 256 kb 的整體屬性集大小限制 (KB) 。

建議 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的執行預設會建立和維護第0版的屬性集。 如果呼叫端隨後要求第1版格式的特定功能，則只應該更新屬性集的版本。 例如，如果撰寫 VT_ARRAY 類型的屬性，或寫入較長的屬性名稱，則執行應該會將屬性集格式更新為第1版。 如果在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的呼叫中指定 PROPSETFLAG_CASE_SENSITIVE 列舉值，就會發生這個指導方針的例外狀況。 在此情況下，必須將屬性集建立為第1版屬性集。

 

 