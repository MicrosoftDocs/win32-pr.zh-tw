---
description: 使用永久性地區設定資料
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: 使用永久性地區設定資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852960"
---
# <a name="using-persistent-locale-data"></a>使用永久性地區設定資料

全球化應用程式通常會保存或傳輸資料，例如，時間和日期。 當您決定應用程式應該如何處理資料持續性時，請記住，從電腦到電腦或應用程式執行之間的資料並不一定相同。 這適用于隨附于 Windows 和[自訂地區](custom-locales.md)設定的兩種[地區](locales-and-languages.md)設定。

應用程式的設計必須考慮各種可能發生的地區設定相關資料變更。 例如：

-   貨幣符號可以隨著國家採用歐元而變更。
-   區域喜好設定可以變更。 例如，d/m/y 格式可能會變更為特定地區設定的 m/d/y 格式。
-   由於拼寫 reforms，可能會變更日名稱的拼寫。 此外，也可以變更月份或日期名稱的大小寫。

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>使用 Locale-Independent 格式進行儲存體和資料交換

保存資料的應用程式應該使用與地區設定無關的儲存和資料交換格式。 範例有硬式編碼或標準格式;非變異地區設定的 [地區設定 \_ 名稱不 \_ 變](locale-name-constants.md); 以及二進位儲存格式。

如果需要持續性排序資料，應用程式必須使用 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) 函數。 請記住，不變的格式不會針對地區設定和行事歷數據進行 [排序](sorting.md)，因此不會維持不變。

## <a name="use-the-user-default-locale-for-data-presentation"></a>使用資料呈現的使用者預設地區設定

若要呈現持續性資料，最適合讓應用程式使用使用者預設地區設定來重新格式化資料。 使用此地區設定可允許使用者覆寫。 如需詳細資訊，請參閱 [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[自訂地區設定](custom-locales.md)
</dt> <dt>

[排序](sorting.md)
</dt> </dl>

 

 



