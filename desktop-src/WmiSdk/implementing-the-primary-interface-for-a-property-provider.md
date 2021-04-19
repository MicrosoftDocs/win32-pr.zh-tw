---
description: 屬性提供者會使用 IWbemPropertyProvider 方法做為 WMI 的主要介面。 您可以使用 IWbemPropertyProvider 來執行程式碼，以取得和修改類別和實例屬性。
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: 執行屬性提供者的主要介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975798"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a>執行屬性提供者的主要介面

屬性提供者會使用 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 方法做為 WMI 的主要介面。 您可以使用 **IWbemPropertyProvider** 來執行程式碼，以取得和修改類別和實例屬性。

下表列出可為屬性提供者執行的 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 方法。



| 方法                                                   | 功能      |
|----------------------------------------------------------|--------------|
| [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | 重建    |
| [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | 修改 |



 

> [!Note]  
> 您必須將屬性提供者實作為同進程提供者。 WMI 將會初始化以服務或可執行檔撰寫的屬性提供者，但永遠不會呼叫其 [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) 和 [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) 方法。

 

如果您選擇不支援其中一種方法，則您的提供者可以提供可傳回 **無法使用 WBEM \_ E \_ 提供者 \_ \_** 的存根執行。

屬性提供者會以三個限定詞的集合來識別 managed 類別或實例： **PropertyCoNtext**、 **InstanceCoNtext** 和 **ClassCoNtext**。 WMI 會將描述這三個限定詞的字串常數傳遞給您的屬性提供者。

您的屬性提供者必須準備好處理下列類型的內容限定詞：

-   **InstanceCoNtext** 辨識符號會附加至實例，並包含適用于實例中每個屬性的資訊。
-   **ClassCoNtext** 限定詞會附加至類別，並包含適用于類別中每個實例的資訊。 例如，在用來儲存登錄提供者所提供之資料的類別中， **ClassCoNtext** 可以是登錄機碼的路徑，其中包含要報告的屬性。
-   **PropertyCoNtext** 限定詞會指定與屬性相關的內容特定資訊。 例如，在用來儲存登錄提供者所提供之資料的類別中， **PropertyCoNtext** 會指定屬性要儲存的登錄值名稱。

這些限定詞可以搭配使用。 您可以同時指定 **InstanceCoNtext** 和 **PropertyCoNtext** 值，告知提供者如何處理特定類型的實例。 例如，您可能想要將提供者辨識的實例標示為可讀取，但只有一個可寫入的屬性。

最常使用的限定詞是 **PropertyCoNtext**。 因此，WMI 會將 **DynProps** 限定詞提供為快捷方式。 WMI 會將以 **DynProps** 標記的實例中的每個屬性，視為也有 **動態**、 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)和 **PropertyCoNtext** 的限定詞。

 

 



