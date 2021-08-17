---
description: 釋放指向 IStream COM 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'ISCardTypeConv：： FreeIStreamMemoryPtr 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 62e91f9d8fca06c812370091b407edb73fed433a4c576857a7e089db28d6d856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922387"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>ISCardTypeConv：： FreeIStreamMemoryPtr 方法

\[**FreeIStreamMemoryPtr** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**FreeIStreamMemoryPtr** 方法會釋放指向 **IStream** COM 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。

## <a name="syntax"></a>語法


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStrm* \[在\]
</dt> <dd>

可管理 *pMem* 所指向之記憶體區塊的 **IStream** 介面指標。

</dd> <dt>

*pMem* \[在\]
</dt> <dd>

由 **IStream** 介面管理之記憶體區塊的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | 描述                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 已成功配置記憶體。<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞至函式的一或多個參數發生問題。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 指標類型的參數不正確。<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 可用記憶體不足，無法滿足要求。<br/>                                            |



 

## <a name="remarks"></a>備註

這個函式會完整且完全釋放指向 **IStream** 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。 呼叫 [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)時，會取得位元組指標。

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
</dt> <dt>

[**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
