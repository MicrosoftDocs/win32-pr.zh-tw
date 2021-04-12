---
description: 在 Windows Vista 和更新版本的屬性系統中所使用的屬性是在屬性架構中宣告的。
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: 建立自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319635"
---
# <a name="creating-custom-properties"></a>建立自訂屬性

在 Windows Vista 和更新版本的屬性系統中所使用的屬性是在屬性架構中宣告的。 這些屬性架構是在 XML 檔案中定義，而且會描述屬性的各個層面，包括它的型別 (包括其基本型別的資訊，以及它是否為多重值) 、如何在 Windows UI 中顯示、哪些標籤 (方便使用的使用者易記編輯) 字串，以及在搜尋存放區中快取的方式，以加快存取的速度。 屬性是透過其正式名稱或其屬性索引鍵 (PKEY) 來識別。

正式名稱是屬性的讀取者易記名稱，並使用類似于 Microsoft .NET 中所使用的命名空間慣例。 如果系統定義的屬性 (Windows) 中所包含的屬性，則慣例為 `System.GroupName.PropertyName` 。 請注意，在每個單字開頭用來將字母大寫的 Pascal 大小寫配置，都是在這些名稱中使用。 標準名稱會用於不同的位置，包括屬性清單和屬性快取中的資料行名稱。 因此，結構化查詢語言 (SQL)  (SQL) 查詢來取得屬性值。

PKEY 是由 GUID 和 **DWORD** 組成的一對值，分別稱為 *formatID* 和 *propID* 。 它是以 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構表示。 大部分的屬性系統 Api 都會接受這些屬性索引鍵。 Windows 軟體開發套件 (SDK) 包含標頭檔 Propkey，其中包含每個屬性索引鍵的巨集定義，以及的 `System` 慣例 `PKEY_GroupName_PropertyName` 。 例如， `PKEY_Photo_DateTaken` 是具有標準名稱之屬性的屬性索引鍵 `System.Photo.DateTaken` 。 屬性值會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構的形式儲存，也就是 OLE 變異類型的延伸。

本節包含下列主題，這是建立自訂屬性的整數：

-   [瞭解屬性描述架構](./propdesc-schema-entry.md)

> [!Note]  
> 由於索引子在取用屬性系統架構時可能會遇到的問題，因此您必須謹慎地定義屬性，並策略性地針對第一版的架構來定義屬性。 在架構註冊之後，資料庫的任何變更 (類型、資料行寬度、indexible) 是否都不會反映在資料庫中。 當架構在系統上註冊一次之後，唯一可辨識這些變更的方法就是重建索引，然後註冊新的架構，或是註冊架構，然後為每個後續的版本建立新的屬性。例如 `PKEY_GroupName_PropertyNameV2` ，等 `PKEY_GroupName_PropertyNameV3`) 。 我們不建議以這種方式建立新的屬性，因為多個額外的資料行可能會影響系統效能。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行屬性處理常式](./building-property-handlers.md)
</dt> <dt>

[屬性描述架構](./propdesc-schema-entry.md)
</dt> </dl>

 

 
