---
description: Clone 方法會使用它自己的 seek 指標來建立新的物件，該物件會參考與原始 IByteBuffer 物件相同的位元組。
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'IByteBuffer：： Clone 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194078"
---
# <a name="ibytebufferclone-method"></a>IByteBuffer：： Clone 方法

\[**複製** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Clone** 方法會使用它自己的 seek 指標來建立新的物件，該物件會參考與原始 [**IByteBuffer**](ibytebuffer.md)物件相同的位元組。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppByteBuffer* \[擴展\]
</dt> <dd>

成功時，指向新資料流程物件之 [**IByteBuffer**](ibytebuffer.md) 指標的位置。 當您完成使用 **IByteBuffer** 指標時，請呼叫 [**IUnknown：： release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 函式來釋放它。 如果發生錯誤，此參數為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

這個方法會建立新的資料流程物件來存取相同的位元組，但使用個別的 seek 指標。 新的資料流程物件會看到與來來源資料流物件相同的資料。 寫入至一個物件的變更會立即顯示在另一個物件中。 範圍鎖定會在資料流程物件之間共用。

複製的資料流程實例中搜尋指標的初始設定，與複製作業時原始資料流程中的搜尋指標目前設定相同。

## <a name="examples"></a>範例

下列範例顯示覆制 [**IByteBuffer**](ibytebuffer.md) 介面。


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardssp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

