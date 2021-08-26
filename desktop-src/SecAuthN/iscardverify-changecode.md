---
description: 以新的 CHV 代碼取代目前的 CHV (卡持有者驗證) 程式碼。
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: ISCardVerify：： ChangeCode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 665cf0ec4c06feca9bcc221125daedc9ab8a12dabed0577b1f4bab5a31334804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013538"
---
# <a name="iscardverifychangecode-method"></a>ISCardVerify：： ChangeCode 方法

\[**ChangeCode** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ChangeCode** 方法會以新的 CHV 程式碼取代目前的 CHV (卡持有者驗證) 程式碼。

## <a name="syntax"></a>語法


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOldCode* \[在\]
</dt> <dd>

[**IByteBuffer**](ibytebuffer.md)的指標，其中包含使用者的目前程式碼。

</dd> <dt>

*pNewCode* \[在\]
</dt> <dd>

包含新程式碼的 [**IByteBuffer**](ibytebuffer.md) 指標，該程式碼會在變更過程中向 [*智慧卡*](../secgloss/s-gly.md) 呈現，以驗證使用者。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指出程式碼為全域或本機，以及程式碼是否應啟用或停用。

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ FL \_ 的 \_ 通用**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ FL \_ 的 \_ 本機 IHV**
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

**SC \_ FL 的 \_ IHV \_ 啟用**
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

**SC \_ FL 的 \_ IHV \_ 停用**
</dt> </dl> </dd> <dt>

*lRef* \[在\]
</dt> <dd>

智慧卡特定參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | 描述                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

如需此介面所定義之所有方法的清單，請參閱 [**ISCardVerify**](iscardverify.md)。

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

[**IByteBuffer**](ibytebuffer.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[智慧卡傳回值](authentication-return-values.md)
</dt> </dl>

 

 
