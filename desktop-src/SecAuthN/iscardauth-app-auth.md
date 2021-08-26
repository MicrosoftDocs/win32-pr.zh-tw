---
description: 應用 \_ 程式驗證方法會驗證應用程式。 它可讓應用程式在智慧卡要求驗證時，使用挑戰/簽章通訊協定) 驗證自己 (。
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: ISCardAuth：： APP_Auth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: db6d2b673caf15d5d15e63894a6c5a589fd2d18ea031a3201a562f255ee6cf2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015548"
---
# <a name="iscardauthapp_auth-method"></a>ISCardAuth：： APP \_ Auth 方法

\[**應用程式 \_ 驗證** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

應用 **程式 \_ 驗證** 方法會驗證應用程式。 它可讓應用程式在 [*智慧卡*](../secgloss/s-gly.md)要求驗證時，使用挑戰/簽章通訊協定) 驗證自己 (。

## <a name="syntax"></a>語法


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lAlgoID* \[在\]
</dt> <dd>

要在驗證程式中使用的演算法。

</dd> <dt>

*pParam* \[在\]
</dt> <dd>

[**IByteBuffer**](ibytebuffer.md) ，其中包含驗證程式的特定廠商參數。

</dd> <dt>

*pBuffer* \[在\]
</dt> <dd>

計算所需的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

如需此介面所提供的所有方法清單，請參閱 [**ISCardAuth**](iscardauth.md)。

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

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
