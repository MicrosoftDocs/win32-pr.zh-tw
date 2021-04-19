---
description: 包含 CryptUIDlgSelectCertificate 函數所顯示之對話方塊的相關資訊。
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: CRYPTUI_SELECTCERTIFICATE_STRUCT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985360"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>CRYPTUI \_ SELECTCERTIFICATE \_ 結構結構

**CRYPTUI \_ SELECTCERTIFICATE \_ 結構** 結構包含 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)函數所顯示之對話方塊的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

此結構的大小（以位元組為單位）。

</dd> <dt>

**hwndParent**
</dt> <dd>

對話方塊的父視窗控制碼。 如果這個值是 **Null**，父視窗就是預設的桌面視窗。

</dd> <dt>

**dwFlags**
</dt> <dd>

指定 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) 函數的其他選項。 這可以是零或下列值的位 **or** 。



| 值                                                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt> </dl>                              | 保留的。<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ 舊版**</dt> </dl>                                       | 指定要顯示舊版對話。<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ 多重複選**</dt> </dl>                        | 允許使用者在對話方塊中選取一個以上的憑證。 如果設定此旗標， [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) 函數一律會傳回 **Null**。 此結構的 **hSelectedCertStore** 成員必須包含憑證存放區的控制碼。 使用者選取的憑證將會新增至此存放區。<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ PUT \_ 視窗 \_ 最上層**</dt> </dl> | 強制密碼編譯 UI 成為畫面上的最上層視窗。<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**szTitle**
</dt> <dd>

對話方塊的顯示標題。 如果此成員的值為 **Null**，則會使用 [選取憑證] 的預設標題。

</dd> <dt>

**dwDontUseColumn**
</dt> <dd>

可以合併以排除顯示之資料行的旗標。



| 值                                                                                                                                                                                                                                                                                       | 意義                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**CRYPTUI \_選取 \_ ISSUEDTO 資料 \_ 行**</dt> <dt>1 (0x1)</dt> </dl>             | 不要顯示 **ISSUEDTO** 資訊。<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**CRYPTUI \_選取 \_ ISSUEDBY 資料 \_ 行**</dt> <dt>2 (0x2)</dt> </dl>             | 不要顯示 **ISSUEDBY** 資訊。<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**CRYPTUI \_選取 \_ INTENDEDUSE 資料 \_ 行**</dt> <dt>4 (0x4)</dt> </dl>    | 不要顯示 **IntendedUse** 資訊。<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**CRYPTUI \_選取 \_ FRIENDLYNAME 資料 \_ 行**</dt> <dt>8 (0x8)</dt> </dl> | 不要顯示名稱資訊。<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**CRYPTUI \_選取 \_ 位置資料 \_ 行**</dt> <dt>16 (0x10)</dt> </dl>           | 不要顯示位置資訊。<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**CRYPTUI \_選取 \_ 到期資料 \_ 行**</dt> <dt>32 (0x20)</dt> </dl>     | 不要顯示到期資訊。<br/>      |



 

</dd> <dt>

**szDisplayString**
</dt> <dd>

對話方塊中顯示的文字，可指示使用者。 如果此成員的值為 **Null**，則會使用預設字串「選取您要使用的憑證」。

</dd> <dt>

**pFilterCallback**
</dt> <dd>

[**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc)回呼函式的指標，該函式會篩選對話方塊中顯示的憑證。

</dd> <dt>

**pDisplayCallback**
</dt> <dd>

[**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)回呼函式的指標，此函式會顯示使用者選取要查看的憑證。

</dd> <dt>

**pvCallbackData**
</dt> <dd>

傳遞給 **pFilterCallback** 和 **pDisplayCallback** 成員所指定之回呼函數的其他資料。

</dd> <dt>

**cDisplayStores**
</dt> <dd>

**RghDisplayStores** 陣列中的憑證存放區數目。

</dd> <dt>

**rghDisplayStores**
</dt> <dd>

存放區陣列的指標，其中包含可在對話方塊中選取的憑證。

</dd> <dt>

**cStores**
</dt> <dd>

**RghStores** 陣列中的憑證存放區數目。

</dd> <dt>

**rghStores**
</dt> <dd>

要在建立憑證鏈時搜尋的憑證存放區陣列的指標，並確認對話方塊中顯示的憑證信任。

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

**RgPropSheetPages** 陣列中的屬性頁數目。

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

**PROPSHEETPAGE** 結構陣列的指標，代表當選取憑證以供查看時，傳遞給憑證查看對話方塊的屬性頁。

</dd> <dt>

**hSelectedCertStore**
</dt> <dd>

呼叫端所建立之憑證存放區的控制碼。 使用者選取的憑證會新增至此存放區。 如果在呼叫 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)之前和之後，此存放區中的憑證數目是相同的，使用者就會關閉對話方塊，而不選取任何憑證。

如果此結構的 **dwFlags** 成員未包含 **CRYPTUI \_ SELECTCERT \_ 多重** 複選旗標，則不會使用這個成員。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                            |
| Unicode 與 ANSI 名稱<br/>   | **CRYPTUI \_SELECTCERTIFICATE \_ STRUCTW** (Unicode) 和 **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




