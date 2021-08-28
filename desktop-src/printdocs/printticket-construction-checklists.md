---
description: 查看 PrintTicket 用戶端的作者如何使用元素類型來建立可描述裝置意圖的 PrintTicket。
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: PrintTicket 結構檢查清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6a3ae0c19fea01738dbf7c6ecfa52f6f156d59f67dae89d6d5a2952059a765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091718"
---
# <a name="printticket-construction-checklists"></a>PrintTicket 結構檢查清單

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

本節將示範 PrintTicket 用戶端的作者如何使用在 Print Schema Framework 中定義的元素類型，來建立可描述裝置意圖的 PrintTicket。 PrintTicket 可以是泛型 (未系結至特定裝置) ，也可以是裝置特定的。 會更詳細地呈現 PrintTicket 的語法。 此外，本節還包含一些概念和術語的總覽，這些概念和術語在後續章節中有更深入的討論。

有兩種本質上不同的方法可以用來建立 PrintTicket。 這兩種方法都可以使用。

-   藉由 [建立一般的 printticket](creating-a-generic-printticket.md)，將 PrintTicket 的目標設為未知或一般裝置。

    如果您的主要目標是要保留使用者的意圖，您可能會想要採用這種方法，方法是使用檔來建立和儲存未經驗證一般 PrintTicket。

-   藉由 [建立 Device-Specific 的 printticket](creating-a-device-specific-printticket.md)，將 printticket 的目標設為特定裝置。

    如果您想要充分利用特定裝置所提供的所有功能，您可能會想要採用這種方法，方法是針對特定裝置建立 PrintTicket，並將驗證的 PrintTicket 與檔一起儲存。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



