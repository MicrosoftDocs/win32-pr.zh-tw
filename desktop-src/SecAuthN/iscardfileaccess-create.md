---
description: Create 方法會在智慧卡檔案系統內的指定位置建立檔案。
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: ISCardFileAccess：： Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: cc6609e2b39c8e0e6b2c034d9220d78b3e28194ca1d92a383236411e77802164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481308"
---
# <a name="iscardfileaccesscreate-method"></a>ISCardFileAccess：： Create 方法

\[**Create** 方法可在 [需求] 區段中指定的作業系統中使用。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Create** 方法會在 [*智慧卡*](../secgloss/s-gly.md)檔案系統內的指定位置建立檔案。

## <a name="syntax"></a>語法


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*refType* \[在\]
</dt> <dd>

*BstrPathSpec* 中使用的參考型別。

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ 類型（ \_ 依 \_ 名稱）**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ 類型（ \_ 依 \_ 識別碼）**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ 類型 \_ （ \_ 簡短）**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ 類型（ \_ 依 \_ 任何**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[在\]
</dt> <dd>

要在目前內容中建立的檔案識別碼。

</dd> <dt>

*TLV* \[在\]
</dt> <dd>

您必須設定哪些值，才能 (標記、長度、值) 結構的 TLV 清單。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指定是否必須使用安全訊息，並預先配置資料。

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ 安全 \_ 訊息**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL 預先配置 \_**
</dt> </dl> </dd> <dt>

*pDataBuffer* \[在\]
</dt> <dd>

預先配置資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
