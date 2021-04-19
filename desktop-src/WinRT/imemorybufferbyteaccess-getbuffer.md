---
description: 取得 IMemoryBuffer，表示為位元組陣列。
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: IMemoryBufferByteAccess：： GetBuffer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973276"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>IMemoryBufferByteAccess：： GetBuffer 方法

取得 [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) ，表示為位元組陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

包含緩衝區資料的位元組陣列指標。

</dd> <dt>

*容量* \[擴展\]
</dt> <dd>

傳回陣列中的位元組數目

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

呼叫 [**MemoryBuffer：： Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) 時，使用這個緩衝區的程式碼應該將 *值* 指標設為 null。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
