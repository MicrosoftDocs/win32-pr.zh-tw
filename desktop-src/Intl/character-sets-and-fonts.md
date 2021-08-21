---
description: Windows 允許雙位元組字元集中非標準字元的本機定義 (dbcs) 與 Unicode。
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: 字元集和字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeee925f55887ac8120474f14b727ea244dc02c3b1e7908f424c0dbf09d502b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068278"
---
# <a name="character-sets-and-fonts"></a>字元集和字型

Windows 允許[雙位元組字元集](double-byte-character-sets.md)中非標準字元的本機定義 (dbcs) 與[Unicode](unicode.md)。 若為 DBCS，這些非標準的字元稱為 (EUDC) 的使用者定義字元。 Unicode 透過其私用區域 (PUA) 提供類似的功能。 應用程式會使用關聯的 DBCS 或 Unicode 字元值來識別指定的字元。

可以指派的 DBCS 字元值取決於指定的字元集。 每個東亞 Windows[字碼頁](code-pages.md)都至少有一個保留值範圍，可作為 EUDCs 使用。 範圍是由 [EUDCCodeRange](eudccoderange.md) 登錄機碼定義。 此用途的 unicode 值一律來自 Unicode PUA、值 U + E000 至 U + F8FF、U + F0000 至 U + FFFFD，以及 U + 100000 至 U + 10FFFD。

若要建立 EUDC 或 PUA 字元，使用者可選擇指定範圍內的字元值，並 [將該字元加入至對應](uniscribe-glossary.md) 至該字元值之專案中的字型。 使用者會使用 EUDC 編輯器或使用從字型廠商購買的字型套件來建立圖像。 任何 DBCS 字型都可以包含 EUDCs，而且任何 Unicode 字型都可以包含 PUA 字元。 如果字型只包含 EUDCs，則該字型稱為「個別」的 EUDC/PUA 字型。 如果字型包含標準字元和 EUDCs，字型就是「整合式」 EUDC/PUA 字型。

系統預設的 EUDC/PUA 字型是一種字型，作業系統會自動與所有 DBCS 和 Unicode 字型產生關聯，但具有明確相關聯的 EUDC/PUA 字型字型除外。 應用程式會設定「 [eudc](eudc.md) 」登錄機碼下的 SystemDefaultEUDCFont 名稱值，以設定系統預設的 EUDC/PUA 字型。 同樣地，應用程式可以在 EUDC 索引鍵下指定字型名稱和相關聯的字型檔案，以將個別的 EUDC/PUA 字型與對應的字型產生關聯。 作業系統一律會先嘗試尋找目前所選字型中的 EUDC/PUA。 如果找不到字型，則作業系統會尋找相關聯的 EUDC/PUA 字型中的字元（如果已定義目前所選字型的字元）。 如果仍然找不到字元，則作業系統會以系統預設的 EUDC/PUA 字型來尋找它。

TrueType 字型可以安裝為 ttf 檔案或 tte 檔案。 由於作業系統會隱藏 tte 檔案，因此應用程式無法使用 GDI API 函式來列舉或檢查已安裝的字型。 在許多作業系統上，系統預設的 EUDC/PUA 字型和個別的 EUDC/PUA 字型會安裝為 tte 檔案。 您必須使用登錄專案來新增、修改和刪除這類字型，像是 EUDC 編輯器和主控台的應用程式必須使用登錄專案。

使用 EUDC 和 PUA 字元並不會在不同的電腦或字元集之間可靠地保留意義。 如需有關使用 EUDC 和 PUA 字元的進一步警告，請參閱 [使用者定義和私用的區域字元](end-user-defined-characters.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[終端使用者定義和私用區域字元](end-user-defined-characters.md)
</dt> </dl>

 

 



