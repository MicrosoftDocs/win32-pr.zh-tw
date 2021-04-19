---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: PrintCapabilities 檔的取用者責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997602"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>PrintCapabilities 檔的取用者責任

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 檔的取用者必須先遵守某些義務，才能使用 PrintCapabilities 檔。 下列需求適用于 PrintCapabilities 檔的用戶端。

-   它們不得拒絕或無法處理任何語法有效的 PrintCapabilities;也就是符合 PrintCapabilities 架構的任何 PrintCapabilities 檔。

-   他們必須能夠解決非預期的私用內容存在或不存在的情況。 這包括私用定義的內容，它會出現在 Print Schema 定義專案的實例內。

-   他們必須能夠解決未存在的選擇性列印架構內容。

-   他們必須留意何時要求新檔。

    -   屬性實例的值與設定相依 (因此，與快照集相依的) 。 當您存取屬性實例時，必須更新快照集。

    -   要複製到 PrintTicket 的功能、選項和 ScoredProperty 實例是以靜態定義為依據。 也就是說，它們不 (，且不能) 依存于裝置設定。 如果您存取這些類型的任何實例，當設定變更時，就不需要取得新的 PrintCapabilities 檔。

-    (UI) 用戶端使用者介面的 PrintCapabilities 取用者必須能夠使用 PrintCapabilities 檔中的資訊來建立使用者介面，並從使用者選取專案中建立有效的 PrintTicket。 這包括知道必須指定哪些 ParameterInit 實例，以及驗證所指定的實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



