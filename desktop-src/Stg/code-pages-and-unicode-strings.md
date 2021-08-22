---
title: 字碼頁和 Unicode 字串
description: 執行 IPropertySetStorage 的另一個考慮是如何將 Unicode 屬性名稱儲存在屬性識別碼 0 (屬性名稱字典) ，而不會使用 Unicode 字串。
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- 字碼頁和 Unicode 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a1d5a830d3d4e2fccbb61563e7a8a0447d74e7c427e5e2e0434e7194a2ad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663598"
---
# <a name="code-pages-and-unicode-strings"></a>字碼頁和 Unicode 字串

執行 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的另一個考慮是如何將 Unicode 屬性名稱儲存在屬性識別碼 0 (屬性名稱字典) ，而不會使用 unicode 字串。

Unicode 正式具有字碼頁值1200。 若要將 Unicode 值儲存在屬性名稱字典中，請針對屬性識別碼1中的整個屬性集 (使用1200的字碼頁值) ，並在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)中缺少 **PROPSETFLAG \_ ANSI** 旗標所指定。 請注意，這會有將所有字串值以 Unicode 儲存在屬性集中的副作用。 在所有字碼頁中，在 **VT \_ LPSTR** 的開頭找到的計數是位元組計數，而非字元計數。 為了提供與舊版用戶端的相容性，這是必要的。

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的複合檔案執行會以 Unicode (字碼頁 1200) 或在目前的系統 ANSI 字碼頁中，完全建立所有新的屬性集。 這是由 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *grfFlags* 參數中的 **PROPSETFLAG \_ ANSI** 旗標缺少或存在所控制。

建立並開啟屬性集作為 Unicode。 若要執行這項操作，請勿在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *grfFlags* 參數中設定 **PROPSETFLAG \_ ANSI** 旗標。 避免使用 **vt \_ LPSTR** 值，而改為使用 **vt \_ LPWSTR** 值。 當屬性設定的字碼頁是 Unicode 時， **VT \_ LPSTR** 字串值會在儲存時轉換成 unicode，並在抓取時轉換回多位元組字元串值。

透過呼叫 [**IPropertyStorage：： Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)來設定 **PROPSETFLAG \_ ANSI** 旗標，以反映基礎字碼頁是否為或不是 Unicode。 請注意，您可以明確讀取屬性識別碼1，以學習字碼頁。

您可以透過呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)來存取屬性識別碼1。 不過，它是唯讀的，而且可能不會以 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)進行更新。 此外，它可能不會使用 [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)來刪除。

 

 




