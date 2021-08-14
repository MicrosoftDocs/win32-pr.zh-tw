---
description: 使指定的檔案 (EF 或 DF) 無效。 使用加速復原之前，其他方法無法存取不正確檔案。
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: ISCardFileAccess：：無效方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0d1ed7aa9bbe69f67c0e4e4b4952e23fbfa75bfca470395d9a36eb6867ab16b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481095"
---
# <a name="iscardfileaccessinvalidate-method"></a>ISCardFileAccess：：無效方法

\[無效 **的方法可** 用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

無效 **方法會** 使指定的檔案 (EF 或 DF) 無效。 使用 [**加速復原**](iscardfileaccess-rehabilitate.md)之前，其他方法無法存取不正確檔案。

## <a name="syntax"></a>語法


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrPathSpec* \[在\]
</dt> <dd>

檔案

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指定是否應使用安全訊息。

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ 安全 \_ 訊息**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 參數無效。<br/>         |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

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
</dt> <dt>

[**恢復**](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
