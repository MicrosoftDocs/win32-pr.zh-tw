---
description: Windows Vista 和更新版本： NLS 除了現有的 Windows 地區設定之外，還定義了數個虛擬地區設定來使用。
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974025"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista 和更新版本：** NLS 除了現有的 Windows 地區設定之外，還定義了數個虛擬地區設定。 使用這些虛擬地區設定來測試應用程式的當地語系化。 如需執行的詳細資訊，請參閱 [使用 Pseudo-Locales 進行當地語系化測試](using-pseudo-locales-for-localization-testing.md)。

## <a name="supported-pseudo-locales"></a>支援的 Pseudo-Locales

NLS 支援的虛擬地區設定如下：

-   基底虛擬-地區設定
-   鏡像 (由右至左) 虛擬地區設定
-   東亞語言虛擬-地區設定

根據其字碼頁指派和當地語系化的字串（例如月份名稱、日期名稱），選擇要使用的特定虛擬地區設定。 每個虛擬地區設定的資料，不僅包含相關的字碼頁，也包括用於當地語系化的日期和月份字串，也包含其他數個 NLS 測試案例的資料。 測試案例會檢查下列資料類型：

-   9位 [地區設定識別碼](locale-identifiers.md)。 虛擬地區設定可讓您更有效地測試9位地區設定識別碼的操作。
-   需要使用小型字型的語言字串。 由於圖形裝置介面 (GDI) 的限制，某些語言的使用者介面字型小於最佳。 虛擬地區設定包含這些語言中的數個字串，並結合了具有更標準字型處理語言的字串。 您可以在測試中使用這些字串來判斷如何轉譯受 GDI 限制的字型。
-   不尋常的字串長度。 某些地區設定資訊常數（例如， [地區設定 \_ SLIST](locale-slist.md) 和 [地區設定 \_ ICURRENCY](locale-icurrency.md)）具有字串大小的傳統限制。 虛擬地區設定支援不同字串長度的檢查。
-   替代排序。 當替代 [排序次序識別碼](sort-order-identifiers.md) 與通常與地區設定相關聯的基底排序次序識別碼不同時，可以使用虛擬地區設定來測試替代排序功能。

## <a name="pseudo-locale-names-and-identifiers"></a>虛擬地區設定名稱和識別碼

虛擬地區設定具有從私用空間選擇的 [地區設定名稱](locale-names.md) ，以避免與國際標準組織中引入的可能字串 (ISO) 639 和 iso 3166 標準發生衝突。 每個虛擬地區設定也都有自己的地區設定識別碼。 下表提供所定義虛擬地區設定的名稱和識別碼。



| 虛擬地區設定       | 地區設定名稱 | 地區設定識別碼 |
|---------------------|-------------|-------------------|
| 基本                | qps-qps-ploc    | 0501              |
| 鏡像            | qps-plocm   | 09ff              |
| 東亞語言 | qps-ploca   | 05fe              |



 

## <a name="example"></a>範例

下列範例會顯示針對基底虛擬地區設定顯示的文字：

\[Шěđлеśđαỳ!!! \] 、8ōf \[ Μäŕςћ！！ \] ōf 2006

## <a name="related-topics"></a>相關主題

<dl> <dt>

[地區設定和語言](locales-and-languages.md)
</dt> <dt>

[地區設定識別碼](locale-identifiers.md)
</dt> <dt>

[地區設定名稱](locale-names.md)
</dt> <dt>

[排序次序識別碼](sort-order-identifiers.md)
</dt> <dt>

[使用 Pseudo-Locales 進行當地語系化測試](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



