---
description: GetChallenge 方法會從智慧卡傳回挑戰。
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: ISCardAuth：： GetChallenge 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0132ab8b4b3b2f646639c1618a9f2ca7e67fad1ce2c2fcec38590c7608802091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015418"
---
# <a name="iscardauthgetchallenge-method"></a>ISCardAuth：： GetChallenge 方法

\[**GetChallenge** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**GetChallenge** 方法會從 [*智慧卡*](../secgloss/s-gly.md)傳回挑戰。

## <a name="syntax"></a>語法


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lAlgoID* \[在中，選擇性\]
</dt> <dd>

要在驗證程式中使用的演算法。

</dd> <dt>

*lLengthOfChallenge* \[在\]
</dt> <dd>

預期回應的最大長度。

</dd> <dt>

*pParam* \[在\]
</dt> <dd>

[**IByteBuffer**](ibytebuffer.md)物件，其中包含驗證程式的特定廠商參數。

</dd> <dt>

*pBuffer* \[in、out\]
</dt> <dd>

在輸入時，指向緩衝區。

在輸出時，會包含來自卡片的挑戰資料。

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
</dt> </dl>

 

 
