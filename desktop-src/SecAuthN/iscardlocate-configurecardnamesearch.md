---
description: ConfigureCardNameSearch 方法會指定要在智慧卡搜尋中使用的卡片名稱。
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'ISCardLocate：： ConfigureCardNameSearch 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193278"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>ISCardLocate：： ConfigureCardNameSearch 方法

\[**ConfigureCardNameSearch** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ConfigureCardNameSearch** 方法會指定要在 [*智慧卡*](../secgloss/s-gly.md)搜尋中使用的卡片名稱。

## <a name="syntax"></a>語法


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCardNames* \[在\]
</dt> <dd>

以 BSTR 形式的卡片名稱之 Automation 安全陣列的指標。

</dd> <dt>

*pGroupNames* \[在\]
</dt> <dd>

以 BSTR 形式的「卡片/讀者」群組名稱的自動化安全陣列指標，可新增至搜尋。

</dd> <dt>

*bstrTitle* \[在\]
</dt> <dd>

搜尋通用控制項的對話方塊標題。

</dd> <dt>

*lFlags* \[在\]
</dt> <dd>

指定何時顯示 [*使用者介面*](../secgloss/u-gly.md) 。



| 值                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**SC \_ DLG \_ 基本 \_ UI**</dt> </dl> | 只有在呼叫的應用程式所搜尋的卡片找不到且無法在讀取器中使用時，才會顯示對話方塊。 如此一來，就可以透過內部對話方塊機制或使用) 的使用者回呼函式，以及傳回給呼叫的應用程式，來找出卡片、連接 (。<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ D \_ 沒有 \_ UI**</dt> </dl>                | 不論搜尋結果為何，都不會顯示任何 UI。<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ FORCE \_ UI**</dt> </dl>       | 不論搜尋結果為何，都會顯示 UI。<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                                         |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *pCardNames* 或 *pGroupNames* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                             |



 

## <a name="remarks"></a>備註

若要找出 [*智慧卡*](../secgloss/s-gly.md)，請呼叫 [**FindCard**](iscardlocate-findcard.md)。

如需此介面所提供的所有方法清單，請參閱 [**ISCardLocate**](iscardlocate.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate 定義為1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
