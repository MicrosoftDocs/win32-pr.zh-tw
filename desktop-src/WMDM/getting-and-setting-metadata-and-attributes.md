---
title: 取得和設定中繼資料和屬性
description: 取得和設定中繼資料和屬性
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows媒體裝置管理員，屬性
- 裝置管理員，屬性
- 桌面應用程式，屬性
- 服務提供者，屬性
- 程式設計指南，屬性
- 屬性
- Windows媒體裝置管理員，中繼資料
- 裝置管理員，中繼資料
- 桌面應用程式，中繼資料
- 服務提供者，中繼資料
- 程式設計指南，中繼資料
- 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c8311c3fff3c4785116604e53652c4f07b6b63b3a2c4389cc3dd4b6a5f35a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957558"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>取得和設定中繼資料和屬性

應用程式可以取得儲存體或裝置的兩種資訊：屬性和中繼資料。 屬性是較簡單的布林值，通常會描述檔案系統資訊，例如儲存體是否有子物件、是否可以重新命名、讀取或刪除等等。 藉由呼叫 [**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) 或 [**IWMDMStorage2：： GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)，可將屬性視為旗標值來取出。 藉由呼叫 [**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)來設定屬性。

應用程式也可以要求更複雜的資料 (數值、字串或) 為 *元* 資料的其他資料類型。 中繼資料值是由唯一的字串名稱所識別。 Windows媒體裝置管理員定義可用來要求值的字串常數清單;這些定義的值會列在[中繼資料常數](metadata-constants.md)中。 服務提供者可以定義自己的常數，但呼叫的應用程式必須知道這些定義，才能要求或設定這些自訂中繼資料值。 應用程式會藉由呼叫 [**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) 或 [**IWMDMStorage4：： GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)來要求中繼資料。

取得和設定中繼資料和屬性的一個重要層面，就是了解抓取值的來源。 服務提供者或裝置可以從許多不同的位置取得這些值，包括下列各項：

-   從檔案標頭。 例如，在 ASF 檔案中，位元速率會儲存在檔案標頭中。
-   從應用程式在呼叫方法時明確設定的值。 這些值可能會儲存在服務提供者或裝置的外部中繼資料存放區中。 當裝置中斷連線或關閉時，此存放區可能會或可能不會保存。 例如，播放次數和使用者星級分級通常會儲存在電腦或裝置的外部商店中。
-   藉由檢查檔案系統所提供的資訊。 例如，檔案是唯讀或資料夾是否有子系。
-   藉由開啟和剖析檔案資料。

請務必瞭解，屬性可能會儲存在檔案標頭中的多個位置 (，也會儲存在本機存放區) 中，而且它可能會或可能無法編輯。 例如，變更檔案描述不一定是持續性;如果服務提供者將描述儲存在本機，則它不會保存在裝置上。 同樣地，如果檔案描述是取自檔案標頭，則只有在服務提供者或裝置開啟並修改標頭資料時，才會有永久性的修改。 大部分的應用程式會藉由變更所需的值來進行最佳嘗試，但不需依賴任何屬性來持續變更。

如需取得和設定值的詳細資訊，請參閱檔中的應用程式開發人員和服務提供者開發人員的適當章節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式和服務提供者的一般工作**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




