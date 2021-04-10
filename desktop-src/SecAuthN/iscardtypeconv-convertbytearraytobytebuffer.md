---
description: 將典型的 C/c + + 位元組陣列轉換成 (IStream 物件) 的通用位元組緩衝區。
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'ISCardTypeConv：： ConvertByteArrayToByteBuffer 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851723"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>ISCardTypeConv：： ConvertByteArrayToByteBuffer 方法

\[**ConvertByteArrayToByteBuffer** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ConvertByteArrayToByteBuffer** 方法會將典型的 C/c + + 位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。

所建立的位元組緩衝區是透過記憶體區塊對應的資料流程。 若要存取或管理緩衝區，請使用 **IStream** 介面所提供的方法。 這個陣列實作為的獨特功能，就是當您呼叫 **IStream：： Release** 方法時，將會為您釋放基礎記憶體。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbyArray* \[在\]
</dt> <dd>

要轉換的位元組陣列指標。

</dd> <dt>

*dwArraySize* \[在\]
</dt> <dd>

要轉換之位元組陣列的大小。

</dd> <dt>

*ppbyBuffer* \[擴展\]
</dt> <dd>

要傳回的 **IStream** 物件指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 已成功配置記憶體。<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞至函式的一或多個參數發生問題。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 指標類型的參數不正確。<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 可用記憶體不足，無法滿足要求。<br/>                                            |



 

## <a name="remarks"></a>備註

配置的記憶體是可移動的。 使用 **IStream：： Release** 方法釋放記憶體。

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

 

 
