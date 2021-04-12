---
description: 屬性集
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: " (DirectShow) 的屬性集"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385675"
---
# <a name="property-sets-directshow"></a> (DirectShow) 的屬性集

Microsoft DirectShow 使用屬性集來支援硬體及其相關驅動程式和篩選器所提供的擴充服務。 硬體和篩選廠商可以將新功能定義為屬性、在屬性集中排列它們，以及發佈這些屬性集的規格。 應用程式開發人員可以使用 [**IKsPropertySet**](ikspropertyset.md) 介面的方法，來判斷驅動程式或篩選器是否支援一組特定的屬性，以及取得或設定這些屬性。

**IKsPropertySet** 所公開的所有方法都需要 **GUID** 來識別屬性集 (*guidPropSet* 參數) ，以及在 *dwPropID* 參數)  (屬性集內識別屬性的 **DWORD** 。 *DwPropID* 參數通常是列舉資料類型的成員。

個別屬性可以有您在 [**IKsPropertySet：： Set**](ikspropertyset-set.md)和 [**IKsPropertySet：： Get**](ikspropertyset-get.md)方法的 *pPropData* 參數中指定的相關資料。 在這些方法中，屬性資料會輸入為的指標 `void` 。 資料類型和資料的意義是在屬性集的定義中指定。

下列各節提供有關 DirectShow 所支援之屬性集的資訊：

-   [**DVD 禁止複製屬性集**](dvd-copy-protection-property-set.md)
-   [**DVD 卡拉卡拉屬性集**](dvd-karaoke-property-set.md)
-   [**DVD 子圖片屬性集**](dvd-subpicture-property-set.md)
-   [外部裝置傳輸屬性集](external-device-transport-property-set.md)
-   [框架逐步執行屬性集](frame-stepping-property-set.md)
-   [釘選屬性集](pin-property-set.md)
-   [**速率變更屬性集**](rate-change-property-set.md)

 

 



