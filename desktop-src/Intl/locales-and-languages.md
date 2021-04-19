---
description: 詞彙 &\# 0034; language&\# 0034; 表示在讀出和寫入通訊中使用的屬性集合。
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: 地區設定和語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973899"
---
# <a name="locales-and-languages"></a>地區設定和語言

「語言」一詞表示在讀出和寫入通訊中所使用的屬性集合。 每種語言都有語言名稱和語言識別項，表示特定 [字碼頁](code-pages.md) (ANSI、DOS、Macintosh) 用來代表作業系統上語言的 [地理位置](table-of-geographical-locations.md) 。 中性語言會以名稱（例如 "en" 代表英文）表示。 有更多地理位置的特定語言可透過包含地區設定和國家/地區資訊的名稱來表示。 例如，地區設定英文 (美國) 的語言名稱為 "en-us"。

「地區設定」是以值清單表示的語言相關使用者喜好設定資訊的集合。 Windows XP 支援150以上的地區設定，而 Windows Vista 支援大約200。 每個地區設定都是由語言和排序次序所定義，而且具有地區設定名稱和地區設定識別碼。 德文 (德國) 的地區設定名稱範例是「de de \_ 電話簿」。

每個作業系統都至少有一個已安裝的地區設定，而且通常會有許多可供使用者選取的地區設定。 除了名稱和識別碼之外，每個地區設定都有與其相關聯的各種資訊。 地區設定資訊 [常數](locale-information-constants.md)中會說明地區設定資訊類型。

作業系統會將地區設定指派給每個執行緒，一開始會指派 [地區設定 \_ 系統 \_ 預設值](locale-system-default.md)所定義的「系統預設地區設定」。 當安裝作業系統時，或當使用者使用主控台的 [地區及語言選項] 部分進行選取時，就會設定此地區設定。 在屬於使用者的進程中執行執行緒時，作業系統會將「使用者預設地區設定」指派給執行緒。 此地區設定是由 [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)所定義。 應用程式可以使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) 函式來明確設定執行緒的地區設定，以覆寫其中一個預設值。

語言的執行需要對應的地區設定。 作業系統會藉由選取與特定語言版本相關聯之地區設定的資料（通常是最廣泛的地區設定），來實行中性語言。

從 Windows Vista 開始，特定語言有可能對應至補充地區設定，這是一種自訂地區設定。 因為補充地區設定全都共用單一地區設定識別碼，所以您的應用程式應該依名稱（而非依識別碼）來處理這些地區設定和對應的語言。

語言概念與地區設定概念密切相關，但這兩個詞彙不可互換。 一般來說，與 [多語系消費者介面](multilingual-user-interface.md) 相關的函式會處理語言，而 NLS 函式則是以地區設定為依據。

這一節涵蓋下列主題：

-   [自訂地區設定](custom-locales.md)
-   [語言識別碼](language-identifiers.md)
-   [語言名稱](language-names.md)
-   [地區設定識別碼](locale-identifiers.md)
-   [地區設定名稱](locale-names.md)
-   [虛擬地區設定](pseudo-locales.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於國家語言支援](about-national-language-support.md)
</dt> <dt>

[字碼頁](code-pages.md)
</dt> <dt>

[地區設定資訊常數](locale-information-constants.md)
</dt> <dt>

[多語系使用者介面](multilingual-user-interface.md)
</dt> <dt>

[地理位置資料表](table-of-geographical-locations.md)
</dt> <dt>

[消費者介面語言管理](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



