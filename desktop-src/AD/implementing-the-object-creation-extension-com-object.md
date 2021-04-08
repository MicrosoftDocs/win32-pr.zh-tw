---
title: 執行物件建立延伸模組 COM 物件
description: 物件建立延伸模組是實作為同進程伺服器的 COM 物件。 主要和次要物件建立延伸模組都必須執行 IDsAdminNewObjExt 介面。
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- 執行物件建立延伸模組 COM 物件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c1a9da94caa300c1277cf6f6030357ca9d573d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023235"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>執行物件建立延伸模組 COM 物件

物件建立延伸模組是實作為同進程伺服器的 COM 物件。 主要和次要物件建立延伸模組都必須執行 [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) 介面。

## <a name="implementing-idsadminnewobjext"></a>執行 IDsAdminNewObjExt

建立物件建立嚮導時，它會呼叫延伸模組的 [**IDsAdminNewObjExt：： Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) 方法，以初始化每個物件建立延伸模組。 **Initialize** 方法會提供包含物件建立所在之容器的相關資訊、新物件的類別名稱，以及 wizard 本身的相關資訊。 如果從現有的物件開始建立新物件時，建立物件建立嚮導， *pADsCopySource* 參數將不會是 **Null**。 在此情況下，擴充功能應該嘗試從複製的物件中取得的資料量，是可行的。

初始化擴充功能之後，就會呼叫 [**IDsAdminNewObjExt：： AddPages**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) 方法。 延伸模組必須在此方法中，將頁面加入至 wizard。 建立 wizard 頁面的方式是填入 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) 結構，然後將此結構傳遞至 [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函數。 然後藉由呼叫在 *lpfnAddPage* 參數中傳遞給 **AddPages** 的回呼函式，將頁面加入至 wizard。

在顯示擴充功能頁面之前，會呼叫 [**IDsAdminNewObjExt：： SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) 。 這會為所建立的物件提供具有 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面指標的擴充功能。

當 [wizard] 頁面顯示時，頁面應該會處理並回應任何必要的 wizard 通知訊息，例如 [**PSN \_ Advanced.field.setactive**](../controls/psn-setactive.md) 和 [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md)。

當使用者完成所有的 wizard 頁面時，嚮導會顯示「完成」頁面，以提供所輸入資料的摘要。 Wizard 會針對每個延伸模組呼叫 [**IDsAdminNewObjExt：： GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) 方法來取得此資料。 **GetSummaryInfo** 方法會提供包含在 [完成] 頁面中顯示之文字資料的 **BSTR** 。 物件建立延伸模組不需要提供摘要資料。 在此情況下， **GetSummaryInfo** 應該會傳回 **E \_ >notimpl**。 每個擴充功能都只會呼叫 **GetSummaryInfo** 一次，而不是針對每個頁面呼叫一次，因此，如果物件建立延伸模組加入了多個頁面，則延伸模組必須將摘要資料合併成一個字串。

當使用者按一下 [完成] 頁面中的 [**完成]** 按鈕時，wizard 會使用 **DSA \_ NEWOBJ \_ CTX \_ PRECOMMIT** 內容來呼叫每個延伸模組的 [**IDsAdminNewObjExt：： WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata)方法。 發生這種情況時，擴充功能應該使用 [**IADs：:P**](/windows/desktop/api/iads/nf-iads-iads-put) 的 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法，將收集的資料寫入適當的屬性。 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)介面會提供給 [**IDsAdminNewObjExt：： SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject)方法中的延伸模組。 延伸模組不應藉由呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)來認可快取的屬性。 當所有屬性都已寫入時，主要物件建立延伸模組會藉由呼叫 **IADs：： SetInfo** 來認可變更。 以下將詳細討論這項資訊。

如果發生錯誤，將會通知擴充功能，並在呼叫 [**IDsAdminNewObjExt：： OnError**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) 方法時發生此錯誤。

## <a name="implementing-a-primary-object-creation-wizard"></a>執行主要物件建立嚮導

主要物件建立 wizard 的執行與次要物件建立嚮導相同，不同之處在于主要物件建立嚮導必須執行一些其他步驟。

在關閉第一頁之前，物件建立嚮導必須建立臨時目錄物件。 若要這樣做，請呼叫 [**IDsAdminNewObjPrimarySite：： CreateNew**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) 方法。 [**IDsAdminNewObjPrimarySite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite)介面的指標是藉由在傳遞至 [**IDsAdminNewObjExt：： Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize)的 [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj)介面上呼叫具有 **IID \_ IDsAdminNewObjPrimarySite** 的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得的。 **CreateNew** 方法會建立新的暫存物件，並針對每個延伸模組呼叫 [**IDsAdminNewObjExt：： SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) 。

當物件建立嚮導包含多個頁面時，系統會執行 [完成] 頁面，以顯示要儲存之物件資訊的摘要。 按一下 [完成] 頁面上的 [ **完成** ] 按鈕時，系統會呼叫每一個物件建立延伸模組的 [**IDsAdminNewObjExt：： WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) 方法，然後將暫存物件認可至持續性記憶體。 但是，如果物件建立嚮導只包含一個頁面，則頁面會有 **[確定** ] 和 [ **取消** ] 按鈕，而不是 [ **上一頁**]、 **[下一頁** ] 和 [ **取消** ] 按鈕，而是在 [wizard] 中找到，而且不提供 [完成] 頁面。 因此，單一頁面物件建立延伸模組 wizard 必須呼叫 [**IDsAdminNewObjPrimarySite：： Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) 來執行寫入和儲存作業。 單一頁面的主要物件建立延伸模組應呼叫 **Commit** 以回應 [**PSN \_ WIZFINISH**](../controls/psn-wizfinish.md) 通知。

因為其他物件建立延伸模組可以將頁面加入至 wizard，所以主要物件建立延伸模組可能不知道在嚮導中是否有一個以上的頁面。 這並不是問題的原因有兩種：首先，如果系統執行「完成」頁面，主要物件建立延伸模組將會收到 [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md) 通知，而不是 **PSN \_ WIZNEXT** 通知。 其次，如果 wizard 包含一個以上的頁面， [**Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) 將會失敗 harmlessly。

 

 