---
description: 為了避免條件約束衝突，PrintTicket 提供者必須支援用戶端用來對其 PrintTicket 執行驗證的驗證。
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: 條件約束和 PrintTicket 驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b973373ca98e25d3a167ff28ab433d6e61821de3be822d0e9a8699a025d71f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939128"
---
# <a name="constraints-and-printticket-validation"></a>條件約束和 PrintTicket 驗證

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

如 PrintCapabilities 架構一節中所述，PrintCapabilities 檔中表示的一些可能設定結果對裝置而言是不正確。 不正確設定會被視為包含 (在) 的 PPD/GPD 檔案領域中的條件約束衝突。 為了避免條件約束衝突，PrintTicket 提供者必須支援 PrintTicket 驗證作業，用戶端會使用該作業來對其 PrintTicket 執行驗證。 此作業應該會偵測指定的設定是否可以在裝置上進行。 如果無法進行設定 (因為指定的功能和選項元素不存在於目前的裝置中，或因為設定受限制) ，所以作業應修改輸入 PrintTicket，使其包含有效且不受限制的設定。 作業可能也會移除或驗證 PrintTicket 中的其他資訊。 請注意，遇到條件約束衝突時，驗證程式代碼必須變更其中一個裝置屬性的設定，以避免條件約束衝突。 [選項定義](option-definitions.md) 會建議應使用設備磁碟機定義評分程式來判斷應變更哪個裝置屬性，以最妥善地保留使用者的原始意圖。 驗證程式代碼可能會將評分程式硬式編碼，以優先使用某個裝置屬性，或使用 PrintTicket 中特定屬性實例所提供的資訊來引導解析度。 由於列印架構關鍵字中未定義任何屬性，因此用戶端可以指定每個裝置屬性的相對優先權，因此其他 PrintTicket 提供者可能會忽略用於此用途的任何私用 PrintTicket 屬性元素。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



