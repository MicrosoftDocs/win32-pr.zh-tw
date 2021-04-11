---
description: 限定的元件是單一層級間接取值的方法，類似于指標。
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: 合格元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849155"
---
# <a name="qualified-components"></a>合格元件

限定的元件是單一層級間接取值的方法，類似于指標。 限定元件主要是用來將具有平行功能的元件群組成類別。 例如，如果 [元件資料表](component-table.md) 中列出的30個元件是當地語系化為30個語言的相同 Microsoft Word 傳真範本，您可以使用 [PublishComponent 資料表](publishcomponent-table.md)，將這些元件一起分組為合格元件的類別。

在元件資料表中輸入限定元件的方式與一般元件相同。 每個元件都必須有唯一的元件識別碼 GUID，以及元件資料表中指定的元件識別碼。 此外，限定的元件會與 PublishComponent 資料表中的分類 GUID 和文字字串辨識符號相關聯。 限定的元件是由類別目錄 GUID 和辨識符號所參考，而限定詞只會指向元件資料表中的一般元件。

例如，限定的元件識別碼 GUID 可指向資源 DLL 的不同語言版本。 在此情況下，當地語系化資源 Dll 的群組包含類別目錄和數值地區設定識別碼 (LCID) 字串通常用來作為限定詞。 開發人員可以撰寫使用這些合格元件的安裝套件，以執行下列動作：

-   使用 [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) 或 [**MSIPROVIDEQUALIFIEDCOMPONENTEX**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) 尋找資源 DLL 特定語言版本的路徑，並安裝該資源。
-   藉由呼叫 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)，判斷所有存在的資源 DLL 語言版本。
-   準備應用程式以支援其他語言。 應用程式的未來語言套件可以使用限定元件來新增更多語言版本的資源 DLL。

如需詳細資訊，請參閱 [使用限定的元件](using-qualified-components.md)。

 

 



