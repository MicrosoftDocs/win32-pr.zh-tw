---
description: 限定元件是間接取值的方法，可用來將具有平行功能的元件群組成類別。
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: 使用限定元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113241"
---
# <a name="using-qualified-components"></a>使用限定元件

限定元件是間接取值的方法，可用來將具有平行功能的元件群組成類別。

若要傳回完整路徑並安裝 [限定的元件](qualified-components.md)，請呼叫 [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) 或 [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)。

若要列舉所有限定的元件限定詞和描述性字串，請呼叫 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)。

**將元件群組在一起成為合格元件類別**

1.  在 [元件資料表](component-table.md) 中，包含在新的限定元件類別中的每個元件都必須有一筆記錄。 撰寫元件資料表中的欄位，與一般元件相同。 請注意，每個限定元件都必須在元件資料表的 [元件識別碼] 資料行中輸入唯一的元件識別碼 GUID。
2.  產生每個限定元件的辨識符號文字字串。 限定詞必須是唯一的文字字串，才能在搜尋限定元件時輕鬆地產生。 例如，如果類別中的元件是以語言限定，則 (LCID 的數值地區設定識別碼) 是合理的辨識符號字串。
3.  在 [PublishComponent 資料表](publishcomponent-table.md) 中為每個限定元件新增記錄。 在 [元件] 資料表的 [元件] 資料行中，輸入合格元件的識別碼至 PublishComponent 資料表的 [元件] 資料 \_ 行。 在 [辨識符號] 資料行中，輸入每個限定元件的辨識符號字串。 輸入要向使用者顯示的當地語系化字串，並將限定的元件描述至選擇性的 AppData 資料行。 說明字串應該放在 AppData 欄位中，例如「法文字典」，而不只是數位 LCID。 在 [功能] 資料行中，輸入使用此元件的功能名稱 \_ 。 此欄位中的功能識別碼也必須列在 [功能資料表](feature-table.md)的 [功能] 資料行中。
4.  為此限定元件類別產生類別 GUID。 這必須是有效的 [GUID](guid.md)。 如果您使用 GUIDGEN 之類的公用程式來產生 GUID，請確定它只包含大寫字母。 針對此類別中的每個限定元件，在 [PublishComponent 資料表](publishcomponent-table.md)的 [元件] 欄位中輸入類別 GUID。

下列範例說明如何將合格元件的「傳真範本」類別撰寫至元件、功能和 PublishComponent 資料表。

[PublishComponent 資料表](publishcomponent-table.md)



| ComponentId                  | Qualifier | AppData             | 功能\_   | 元件\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {傳真範本類別 GUID} | 1033      | 美式英文範本 | FAXTemplate | FAXTemplateENU |
|                              | 1041      | 日文範本   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | 泰文範本       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | 德文範本     | FAXTemplate | FAXTemplateDEU |



 

[元件資料表](component-table.md) (部分資料表) 



| 元件      | ComponentId                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*FAX Template (US 英文) 元件 GUID*} |
| FAXTemplateJPN | {*FAX Template (日文) 元件 GUID*}   |
| FAXTemplateTHA | {*FAX Template (泰文) 元件 GUID*}       |
| FAXTemplateDEU | {*FAX Template (德文) 元件 GUID*}     |



 

[功能表](feature-table.md) (部分資料表) 



| 功能     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



