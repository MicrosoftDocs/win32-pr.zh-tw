---
title: 目錄物件選擇器
description: '[目錄物件選擇器] 對話方塊可讓使用者從通用類別目錄、網域或電腦或工作組中選取一個或多個物件。'
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- 目錄物件選擇器廣告
- 物件選擇器廣告
- 物件廣告，物件選擇器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6ba7fd053aa8ab3245bf72c693f0a887aa983
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023253"
---
# <a name="directory-object-picker"></a>目錄物件選擇器

[目錄物件選擇器] 對話方塊可讓使用者從通用類別目錄、網域或電腦或工作組中選取一個或多個物件。 使用者可以選取的物件類型包括使用者、連絡人、群組和電腦物件。 如需 Active Directory Domain Services 的詳細資訊，請參閱 [Active Directory Domain Services](active-directory-domain-services.md)。

若要顯示 [物件選擇器] 對話方塊：

1.  呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) 函數來建立 [**IDsObjectPicker**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker) 介面的實例。
2.  呼叫 [**IDsObjectPicker：： initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) 方法來初始化對話方塊。
3.  呼叫 [**IDsObjectPicker：： InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) 方法以顯示對話方塊。
4.  呼叫 [物件選擇器] 對話方塊所傳回之 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)實例的 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) DSOP 方法，以抓取 [**CFSTR \_ \_ DS \_ 選擇 \_ 清單**](cfstr-dsop-ds-selection-list.md)資料。 **CFSTR \_ DSOP \_ ds \_ 挑選清單剪貼 \_ 簿** 格式會提供包含 [**DS \_ 選擇 \_ 清單**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)結構的 **HGLOBAL** 。 **DS \_ 選擇 \_ 清單** 結構包含在 [物件選擇器] 對話方塊中選取之專案的相關資料。

如果物件需要 (SID) 的安全識別碼，則應該直接從物件選擇器要求這項功能，方法是將 **objectSID** 屬性新增至要針對所選物件取得的屬性清單。 不建議將傳回的物件名稱傳遞給 [**LsaLookupNames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) 或 [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 函數，因為名稱查閱會是多餘的，而且在某些情況下可能會失敗。

如果將儲存任何所選物件的參考，則不應儲存分辨名稱，因為物件可能會移動、重新命名或可能因為地區設定差異而變更。 針對安全性主體，應該針對物件要求 **objectSID** 並安全地儲存。 如果稍後需要安全性主體的名稱，則可以使用 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) 函式來取出。 若為所有其他物件，則應要求和儲存 **objectGUID** 。

## <a name="initialization"></a>初始化

初始化 [物件選擇器] 對話方塊時，會指定一組範圍類型和篩選。 指定的範圍類型可決定使用者可以從中選取物件的位置、網域或電腦。 篩選準則會決定使用者可以從指定範圍類型中選取的物件類型。 如需詳細資訊，請參閱下方的範圍和篩選一節。

依預設，使用者可以在 [目錄物件選擇器] 對話方塊中選取單一物件。 若要啟用多個選取專案，請在對話方塊初始化時，于 [**DSOP \_ INIT \_ 資訊**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info)結構的 **flOptions** 成員中設定 **DSOP \_ 旗 \_** 標。

## <a name="scopes-and-filters"></a>範圍和篩選器

[ **查詢** ] 下拉式清單包含使用者可以從中選取物件的範圍。 範圍是儲存相關資料的網域、電腦、工作組或通用類別目錄，並可讓您存取一組可用的物件。 範圍清單中的專案取決於 [**IDsObjectPicker：： initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) 方法上次呼叫以初始化 [物件選擇器] 對話方塊時所指定的範圍類型和目的電腦。

範圍類型是範圍的一般分類，例如目的電腦所屬企業中的所有網域，或是目的電腦的企業的通用類別目錄或目的電腦本身。 針對每個指定的範圍類型，此對話方塊會使用目的電腦的內容來判斷範圍清單專案。

[**IDsObjectPicker：： Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize)方法會採用 [**DSOP \_ init \_ 資訊**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info)結構的指標，該結構包含 [**DSOP \_ 領域 \_ 初始 \_ 資訊**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info)結構的陣列。 **DSOP \_ 範圍 \_ INIT \_ INFO** 陣列中的每個專案會指定一或多個範圍類型，以及適用的篩選準則和其他屬性。 篩選準則會決定使用者可以從指定範圍類型中選取的物件類型，例如使用者、群組、連絡人和電腦。 當使用者從清單中選取範圍時，對話方塊會套用該範圍類型的篩選器，以顯示可供使用者選取的物件清單。

每個 [**DSOP \_ 範圍的 \_ 初始 \_ 資訊**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) 結構都包含 [**DSOP \_ 篩選 \_ 旗標**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) 結構，以指定該範圍類型的篩選。 **DSOP \_ 篩選 \_ 旗標** 結構可區分上層層級和下層範圍：

-   高層級範圍是通用類別目錄或支援 ADSI [LDAP 提供者](/windows/desktop/ADSI/adsi-ldap-provider)的網域。
-   下層範圍包含工作組和所有個別的電腦。 此對話方塊會使用 ADSI WinNT 提供者來存取舊版的範圍。

[**DSOP \_ 篩選 \_ 旗標**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags)結構中定義了兩組篩選準則旗標：一個用於上層範圍，另一個用於下層範圍。 **DSOP \_ 篩選 \_ 旗標** 結構的 **上層** 成員是 [**DSOP \_ 上層 \_ 篩選 \_ 旗標**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags)結構，可指定高層級範圍的篩選準則。 **DSOP \_ 篩選 \_ 旗標** 結構的 **flDownlevel** 成員是一組旗標，用來指定下層範圍的篩選準則。

 

 