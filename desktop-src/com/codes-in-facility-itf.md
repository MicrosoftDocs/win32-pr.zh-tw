---
title: FACILITY_ITF 中的代碼
description: 設備 ITF 中的代碼 \_
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2a16d051c352c353376865265c0451014f6110fbcde326914c3cc244a36223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793788"
---
# <a name="codes-in-facility_itf"></a>設備 ITF 中的代碼 \_

具有設備（例如設備 \_ Null 和設備 RPC）的 HRESULT \_ 具有通用意義，因為它們定義于單一來源： Microsoft。 但是， 設備 \_ ITF 中的 HRESULT 會由傳回它們的函式或介面方法來決定。 這表示， \_ 從兩個不同介面方法傳回的設備 ITF 中相同的32位值可能會有不同的意義。

設備 ITF 中的 **hresult** 的原因在 \_ 不同的介面中可能會有不同的意義，因為 **hresult** 會保持為有效率的資料類型大小32位。 可惜的是，32位不夠大，無法開發錯誤碼配置系統，以避免不同的程式設計人員在不同位置的不同時間所配置的衝突程式碼 (與) 介面識別碼和 Clsid 的處理方式不同。 因此，32位 **HRESULT** 是結構化的，因此 Microsoft 可以定義數個通用錯誤碼，而讓其他程式設計人員可以定義新的錯誤碼，而不會擔心衝突。 狀態碼慣例如下所示：

-   只有 Microsoft 才能定義設備 ITF 以外設施中的狀態碼 \_ 。
-   設備設施 ITF 中的狀態碼 \_ 是由傳回狀態碼之介面或函式的開發人員唯一定義。 為了避免衝突的錯誤碼，定義介面的人員必須負責協調和發佈 \_ 與該介面相關聯的設施 ITF 狀態碼。

所有的 COM 定義設備 \_ ITF 碼都有 0x0000-0x01FF 範圍內的代碼值。 雖然在設備 ITF 中使用任何程式碼是合法的 \_ ，但建議您只使用 0x0200-0xffff 範圍內的程式碼值。 這項建議是為了減少與任何 COM 定義錯誤混淆的方式。

此外，也建議開發人員定義新的函式和介面，以傳回 COM 和設備 ITF 以外設備中的錯誤碼 \_ 。 尤其是，未來有機會使用 RPC 進行遠端處理的介面，應該將設備的 \_ RPC 代碼定義為合法。 電子 \_ 非預期的是，大部分的開發人員都想要進行普遍合法的特定錯誤碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的錯誤處理](error-handling-in-com.md)
</dt> </dl>

 

 




