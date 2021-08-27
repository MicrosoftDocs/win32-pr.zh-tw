---
description: 建立對應至 IStream (IByteBuffer) 物件的通用位元組緩衝區。
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'ISCardTypeConv：： CreateByteBuffer 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e95ab8989027cb79dfd48720b08d27042c7bd8f9252d1438152dafbae017d762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922407"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>ISCardTypeConv：： CreateByteBuffer 方法

\[**CreateByteBuffer** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**CreateByteBuffer** 方法會建立對應至 **IStream** ([**IByteBuffer**](ibytebuffer.md)) 物件中的通用位元組緩衝區。

所建立的位元組緩衝區是透過記憶體區塊對應的資料流程。 若要存取或管理緩衝區，請使用 **IStream** 介面所提供的方法。 這個陣列實作為的獨特功能，就是當您呼叫 **IStream：： Release** 方法時，將會為您釋放基礎記憶體。

## <a name="syntax"></a>語法


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwAllocSize* \[在\]
</dt> <dd>

要為數組配置的記憶體大小（以位元組為單位）。

</dd> <dt>

*ppbyBuff* \[擴展\]
</dt> <dd>

要傳回的 IStream 物件指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

可能的傳回值如下：



| 傳回碼                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 已成功配置記憶體。<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞至函式的一或多個參數發生問題。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 可用記憶體不足，無法滿足要求。<br/>                                            |



 

## <a name="remarks"></a>備註

配置的記憶體是可移動的。 使用 **IStream：： Release** 方法釋放記憶體。

若要建立一般 C/c + + 位元組陣列，請呼叫 [**CreateByteArray**](iscardtypeconv-createbytearray.md)。

若要建立不帶正負號字元的自動化 SAFEARRAY (bytes) ，請呼叫 [**CreateSafeArray**](iscardtypeconv-createsafearray.md)。

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

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateSafeArray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
