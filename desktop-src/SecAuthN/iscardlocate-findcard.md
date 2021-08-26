---
description: FindCard 方法會搜尋智慧卡，並對其開啟有效的連接。
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'ISCardLocate：： FindCard 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a0db06f9dcafd211f628eb7cd0be9ed2f800b6f1b980d8e2320cd82b2849d386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014238"
---
# <a name="iscardlocatefindcard-method"></a>ISCardLocate：： FindCard 方法

\[**FindCard** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**FindCard** 方法會搜尋 [*智慧卡*](../secgloss/s-gly.md)，並對其開啟有效的連接。

## <a name="syntax"></a>語法


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ShareMode* \[在\]
</dt> <dd>

當開啟連接時，要在其中共用或不共用智慧卡的模式。



| 值                                                                                                                                            | 意義                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**獨家**</dt> </dl> | 沒有其他人使用此智慧卡連線。<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**共用**</dt> </dl>          | 其他應用程式可以使用此連接。<br/>        |



 

</dd> <dt>

*通訊協定* \[在\]
</dt> <dd>

連接到卡片時要使用的通訊協定。

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[在\]
</dt> <dd>

指定何時顯示 [*使用者介面*](../secgloss/u-gly.md) ：



| 值                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**SC \_ DLG \_ 基本 \_ UI**</dt> </dl> | 只有在呼叫的應用程式所搜尋的卡片找不到且無法在讀取器中使用時，才會顯示對話方塊。 如此一來，就可以透過內部對話方塊機制或使用) 的使用者回呼函式，以及傳回給呼叫的應用程式，來找出卡片、連接 (。<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ D \_ 沒有 \_ UI**</dt> </dl>                | 不論搜尋結果為何，都不會顯示任何 UI。<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ FORCE \_ UI**</dt> </dl>       | 不論搜尋結果為何，都會顯示 UI。<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[擴展\]
</dt> <dd>

指向資料結構指標的指標，該結構包含或傳回已開啟 [*智慧卡*](../secgloss/s-gly.md)的相關資訊（如果成功）。 如果作業失敗，則為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                        |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppCardInfo* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                            |



 

## <a name="remarks"></a>備註

若要設定搜尋的搜尋條件，請呼叫 [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) 來指定智慧卡的卡片名稱。

如需此介面所提供的所有方法清單，請參閱 [**ISCardLocate**](iscardlocate.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate 定義為1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
