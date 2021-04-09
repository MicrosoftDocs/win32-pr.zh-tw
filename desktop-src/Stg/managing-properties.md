---
title: 管理屬性
description: 每個屬性都包含屬性（property）識別碼 (在其屬性集) 中是唯一的、variant 型別 (VT 或 VarType) 標記（代表值的型別）和值本身。
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- 結構化儲存體 Strctd Stg.，使用，管理屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10dd78a1f8a8484090728dba6fe149840e940461
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842420"
---
# <a name="managing-properties"></a>管理屬性

每個屬性都包含屬性（property） *識別碼* (在其屬性集) 中是唯一的、 *variant 型別 (VT 或 VarType) 標記* （代表值的型別）和 *值* 本身。 Variant 類型標記描述值中資料的標記法。 此外，也可以將可以用來識別屬性的 *字串名稱* 指派給屬性，而不是使用所需的數值屬性識別碼 (識別碼) 。 為了建立及管理屬性，COM 會定義 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面包括讀取和寫入屬性（property）或屬性（property）名稱陣列的方法。 介面包括與相同名稱的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)方法類似的 [**認可**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)和 [**還原**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)方法。 有公用程式方法可讓您設定屬性集 (CLSID) 的類別識別碼、設定與集合相關聯的時間，以及取得屬性集的相關統計資料。 最後， [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) 方法會建立列舉值，並傳回其 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 介面的指標。 您可以呼叫這個介面的方法來列舉物件上的 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構，以提供目前屬性集中所有屬性的相關資訊。

以下是如何表示屬性的範例。 如果屬性集內的特定屬性保存動物的科學名稱，則該名稱可能會儲存為以零結尾的字串。 連同名稱一起儲存會是一個型別指標，表示值是以零結尾的字串。 這些屬性可能具有下列特性：



| 屬性識別碼 | 字串識別碼 | 類型指標 | 表示的值              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | PID \_ ANIMALNAME   | VT \_ LPWSTR     | 以零結束的 Unicode 字串 |
| 03          | PID \_ LEGCOUNT     | VT \_ I2         | WORD                           |



 

任何辨識屬性集格式的應用程式（透過其格式識別碼 (FMTID) ），都可以查看識別碼為 PID ANIMALNAME 的屬性 \_ ，並判斷它是以零結尾的字串，並讀取和寫入值。 雖然應用程式可以呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 來讀取任何或所有屬性集 (先取得) 的指標，但應用程式必須知道如何解讀屬性集。

屬性值會透過屬性介面傳遞為 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)類型的實例。

請務必區分這些儲存 (持續性) 屬性和執行時間屬性。 Variant 類型值常數的名稱開頭為 VT \_ 。 不過，有效的 PROPVARIANTs 集並非完全等同于自動化和 ActiveX 控制項中所使用的一組 Variant。

這兩個結構之間的唯一差異是每個結構中允許的一組 VT \_ (Variant 類型/VarType) 標記。 在變數和 PROPVARIANT 中可使用特定屬性類型的情況下， (VT 值的型別標記 \_) 一律具有相同的值。 此外，針對指定的 VT \_ 值，variant 和 PROPVARIANTs 中使用的記憶體中標記法相同。 這種方法可讓型別系統捕捉不允許的型別標籤，同時讓熟悉的用戶端在適當的情況下執行指標轉換。

如需詳細資訊，請參閱下一節的 [屬性儲存體考慮](property-storage-considerations.md)。

 

 