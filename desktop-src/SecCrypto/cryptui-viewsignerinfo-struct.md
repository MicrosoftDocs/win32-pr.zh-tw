---
description: 包含 CryptUIDlgViewSignerInfo 函數的資訊。
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026740"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>CRYPTUI \_ VIEWSIGNERINFO \_ 結構結構

\[您可以在 [需求] 區段中指定的作業系統中使用 **CRYPTUI \_ VIEWSIGNERINFO \_ 結構** 結構。 它在後續版本中可能會變更或無法使用。\]

**CRYPTUI \_ VIEWSIGNERINFO \_ 結構** 結構包含 [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)函數的資訊。

> [!Note]  
> 未在已發行的標頭檔中宣告此結構。 若要使用此結構，請使用所示的確切格式來宣告。

 

## <a name="syntax"></a>語法


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

此結構的大小（以位元組為單位）。

</dd> <dt>

**hwndParent**
</dt> <dd>

要作為對話方塊父系的視窗控制碼。 如果對話方塊應該沒有父系，這個成員可以是 **Null** 。

</dd> <dt>

**dwFlags**
</dt> <dd>

一組旗標，可修改 [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) 函式的行為。 目前沒有定義任何旗標，所以此成員必須為零。

</dd> <dt>

**szTitle**
</dt> <dd>

以 null 結束的字串指標，其中包含要在對話方塊中顯示的標題。 如果這個成員是 **Null**，則會使用預設標題。

</dd> <dt>

**pSignerInfo**
</dt> <dd>

[**CMSG \_ 簽署者 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info)結構的指標，其中包含要顯示的簽署者資訊。

</dd> <dt>

**hMsg**
</dt> <dd>

將簽署者資訊解壓縮來源的訊息控制碼。

</dd> <dt>

**pszOID**
</dt> <dd>

以 null 結束的 ANSI 字串指標，其中包含 [*物件識別碼*](../secgloss/o-gly.md) 的字串表示 (OID) ，表示應該驗證簽署的憑證。 例如，如果呼叫此方法來查看 [*憑證信任清單*](../secgloss/c-gly.md) 的簽章 (CTL) ，則應該傳入 **szOID 的 \_ KP \_ CTL \_ 使用方式 \_ 簽署** OID 字串。 如果這個成員是 **Null**，則不會驗證憑證的使用方式。

</dd> <dt>

**>dwreserved**
</dt> <dd>

目前未使用這個參數。 此成員必須是 **Null**。

</dd> <dt>

**cStores**
</dt> <dd>

**RghStores** 陣列中的元素數目。

</dd> <dt>

**rghStores**
</dt> <dd>

**HCERTSTORE** 值的陣列，表示用來搜尋簽署訊息之憑證的其他憑證存放區。 如果這個成員是 **Null**，則不會搜尋其他存放區。 **CStores** 成員包含這個陣列中的元素數目。

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

**RgPropSheetPages** 陣列中的元素數目。

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

[**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2)結構指標的陣列，可定義要在標準對話方塊中顯示的任何額外頁面。 如果這個成員是 **Null**，則不會顯示任何其他頁面。 **CPropSheetPages** 成員包含這個陣列中的元素數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                      |
| Unicode 與 ANSI 名稱<br/>   | **CRYPTUI \_VIEWSIGNERINFO \_ STRUCTW** (Unicode) 和 **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
