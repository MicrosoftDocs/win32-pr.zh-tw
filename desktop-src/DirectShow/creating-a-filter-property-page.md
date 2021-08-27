---
description: 建立篩選屬性頁
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: 建立篩選屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d891c42a6cdb2f1c636278a8270fb13a69580697a31fe78f2f3687246f20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108258"
---
# <a name="creating-a-filter-property-page"></a>建立篩選屬性頁

本節說明如何使用 [**CBasePropertyPage**](cbasepropertypage.md)類別，建立自訂 DirectShow 篩選的屬性頁。 本節中的範例程式碼會顯示建立屬性頁所需的所有步驟。 此範例會顯示可支援飽和度屬性之假設性影片效果篩選的屬性頁。 屬性頁有一個滑杆，可讓使用者移動以調整篩選的飽和度層級。

本節包含下列主題：

-   [步驟1。定義用來設定屬性的機制](step-1--define-a-mechanism-for-setting-the-property.md)
-   [步驟2。執行 ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [步驟3。支援 QueryInterface](step-3--support-queryinterface.md)
-   [步驟4：建立屬性頁](step-4--create-the-property-page.md)
-   [步驟5。將指標儲存至篩選](step-5--store-a-pointer-to-the-filter.md)
-   [步驟6：初始化對話方塊](step-6--initialize-the-dialog.md)
-   [步驟7：處理視窗訊息](step-7--handle-window-messages.md)
-   [步驟8。套用屬性變更](step-8--apply-property-changes.md)
-   [步驟9。中斷屬性頁面的連線](step-9--disconnect-the-property-page.md)
-   [步驟10。支援 COM 註冊](step-10--support-com-registration.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



