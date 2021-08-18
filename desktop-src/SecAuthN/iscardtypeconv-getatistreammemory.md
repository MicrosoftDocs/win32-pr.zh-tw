---
description: 取得由 IStream COM 介面管理的 HGLOBAL 記憶體區塊的位元組指標。
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'ISCardTypeConv：： GetAtIStreamMemory 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6520b9af0cf8f322045dfbe92ffc66ef624eadfa7b1beef0f528c6b299d1c2bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922397"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>ISCardTypeConv：： GetAtIStreamMemory 方法

\[**GetAtIStreamMemory** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**GetAtIStreamMemory** 方法會取得 **IStream** COM 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。

這是取得 **IStream** 下記憶體的方法，不需要取得記憶體區塊的 sizeof 值（以位元組為單位），並使用 **IStream** 介面將位元組讀入暫存位元組陣列中。

## <a name="syntax"></a>語法


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStrm* \[在\]
</dt> <dd>

可管理 HGLOBAL 記憶體區塊的 **IStream** COM 介面指標。

</dd> <dt>

*ppMem* \[擴展\]
</dt> <dd>

如果成功，則為 HGLOBAL 記憶體區塊第一個位元組的指標;否則，如果作業失敗，則 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 已成功配置記憶體。<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞至函式的一或多個參數發生問題。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 指標類型的參數不正確。<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 可用記憶體不足，無法滿足要求。<br/>                                            |



 

## <a name="remarks"></a>備註

每個取得的 *ppMem* 指標都會遞增 **IStream** 參考計數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
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

 

 
