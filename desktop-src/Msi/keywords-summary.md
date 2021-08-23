---
description: 安裝資料庫或轉換中的關鍵字摘要屬性包含關鍵字清單。
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: 關鍵字摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a572161e440b440010d43f598e2baa453dbca514d71aa6f0f672deb7c726fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680308"
---
# <a name="keywords-summary-property"></a>關鍵字摘要屬性

安裝資料庫或轉換中的 **關鍵字摘要** 屬性包含關鍵字清單。 檔案瀏覽器可以使用關鍵字來搜尋檔案的關鍵字。 此屬性包含修補程式套件中修補程式來源的清單。

它是由安裝資料庫、轉換或修補套件的作者所組成，以提供摘要資訊中這個屬性的值。 作者應該執行下列動作，以判斷正確的值。

-   在安裝套件中，將這個屬性的值設定為關鍵字清單。 關鍵字應包含「安裝程式」和產品特定關鍵字，而且可能會進行當地語系化。
-   在轉換中，將這個屬性的值設定為關鍵字清單。 關鍵字應包含「安裝程式」和產品特定關鍵字，而且可能會進行當地語系化。
-   在修補程式套件中，將這個屬性的值設定為修補程式來源的網路或 URL 位置清單（以分號分隔）。 安裝修補程式之後，安裝程式會將這些修補程式新增至修補套件的來源清單。 如果快取的 patch 遺失，安裝程式就可以在原始位置中搜尋來源、 **關鍵字摘要** 屬性加入來源清單中的位置，或是使用 [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) 或 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) 函式新增至來源清單的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




