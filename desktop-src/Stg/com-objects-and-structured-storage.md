---
title: COM 物件和結構化儲存體
description: 持續性屬性最常見的其中一個用途是使用它們來儲存與該物件相關之系統物件（例如檔）的資料。
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- COM 物件和結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4c1405ddfaa060aa249090fc58b25b294a8c9aecc5f7b885d21b55bc162198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663588"
---
# <a name="com-objects-and-structured-storage"></a>COM 物件和結構化儲存體

持續性屬性最常見的其中一個用途是使用它們來儲存與該物件相關之系統物件（例如檔）的資料。 當然，有可能會使用任何物件（例如印表機）來儲存屬性，因此只需要查看其屬性，即可判斷其位置、類型等等。 使用者物件可以有一個屬性集，其中包含 [名字]、[姓氏]、[Office] 和 [電話] 等資料。 您可以撰寫應用程式，以根據物件的屬性查詢全系統的物件集合，例如，顯示位於特定大樓的所有印表機。 不過，目前的系統最常使用檔的屬性。

COM 定義的主要屬性集標準是 [摘要資訊屬性集](the-summary-information-property-set.md)。 這個屬性集既簡單又常用。 應用程式所建立的大部分檔都有一組共同的屬性，適用于這些檔的使用者。 這些屬性包括檔作者的名稱、檔的主旨、建立時等等。 另外還有兩個屬性集是針對 Microsoft Office 95、Office 97 和更新版本所定義。 這些是 [COM 檔摘要] 屬性集和 [User-Defined 屬性] 屬性集。 如需詳細資訊，請參閱[結構化儲存體序列化的屬性集格式](structured-storage-serialized-property-set-format.md)。

在 Windows 3.1 中，每個應用程式都有不同的方式可將此資料儲存在其檔中。 若要檢查給定檔的摘要資訊，使用者必須執行建立檔的應用程式，開啟它，然後叫用 [應用程式摘要資訊] 對話方塊，讓應用程式只顯示其摘要資訊。

COM 屬性集和屬性集介面可讓您在不執行建立應用程式的情況下查看檔案屬性。 例如，所有版本的 Microsoft Word 6.0 或更新版本，以及許多其他已啟用 COM 的應用程式現在會使用 com 結構化儲存體和此處所述的屬性集標準來儲存檔。 因此，其他 Office Suite 應用程式可以顯示[該檔案的摘要資訊屬性集](the-summary-information-property-set.md)，只要該檔案是 com 結構化儲存體檔案，而且建立的應用程式將資訊儲存為 com 屬性集格式即可。 例如，Windows 95 或 Windows 98 shell 會使用這種方式，並可讓使用者直接從 shell 查看任何文字6.0 或更新版本檔的屬性。

若要使用其他應用程式的屬性集，其他應用程式必須辨識如何解讀屬性集內的屬性，這表示標準。 COM 藉由定義一個標準屬性集（即 COM 摘要資訊屬性集）來採用此方法。 任何具有這個屬性集定義的應用程式，都可以輕鬆地存取使用該屬性集規格之 COM 應用程式所建立之任何檔中包含的摘要資訊。

 

 




