---
description: 決定 IStream COM 介面的大小（以位元組為單位）。
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'ISCardTypeConv：： SizeOfIStream 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ec150fdf5a6f296b5728131cd59bb6863016fe46fe0769e6159e43b236f77a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013688"
---
# <a name="iscardtypeconvsizeofistream-method"></a>ISCardTypeConv：： SizeOfIStream 方法

\[**SizeOfIStream** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**SizeOfIStream** 方法會決定 **IStream** COM 介面的大小（以位元組為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStrm* \[在\]
</dt> <dd>

**IStream** COM 介面的指標。

</dd> <dt>

*puliSize* \[擴展\]
</dt> <dd>

不帶正負號的大整數指標，可保存 **IStream** COM 介面的整個64位 sizeof 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | 描述                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 函數 succeeded 和 *\* PuliSize* 是 IStream COM 介面的大小（以位元組為單位）。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 發生未指定的失敗。<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PuliSize* 參數不正確。<br/>                                                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | *PStrm* 參數不正確。<br/>                                                          |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生未預期的錯誤。<br/>                                                                   |



 

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

 

 
