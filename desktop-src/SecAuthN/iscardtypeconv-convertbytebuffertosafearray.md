---
description: 將位元組 (IStream 物件) 的通用緩衝區轉換成不帶正負號 char (byte) 的 SAFEARRAY。
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'ISCardTypeConv：： ConvertByteBufferToSafeArray 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693496"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a>ISCardTypeConv：： ConvertByteBufferToSafeArray 方法

\[**ConvertByteBufferToSafeArray** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ConvertByteBufferToSafeArray** 方法會將位元組 (**IStream** 物件) 的通用緩衝區轉換成不帶正負號 char (byte) 的 SAFEARRAY。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbyBuffer* \[在\]
</dt> <dd>

要轉換之 **IStream** 物件的指標。

</dd> <dt>

*ppbyArray* \[擴展\]
</dt> <dd>

要傳回之 SAFEARRAY 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 已成功配置記憶體。<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞至函式的一或多個參數發生問題。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 指標類型的參數不正確。<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 可用記憶體不足，無法滿足要求。<br/>                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scarddat。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scarddat .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[智慧卡傳回值](authentication-return-values.md)
</dt> </dl>

 

 
