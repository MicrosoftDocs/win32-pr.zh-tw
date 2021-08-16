---
description: GetConnectedMediaType 方法會在範例提取的輸入 pin 上抓取連接的媒體類型。
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'ISampleGrabber：： GetConnectedMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 03dc0c9763bdea75569f9447becb749bf284ae2ad7d77427f6dfc2f0aac58382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818057"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>ISampleGrabber：： GetConnectedMediaType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetConnectedMediaType`方法會在範例提取的輸入釘選上抓取連接的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pType* 
</dt> <dd>

由呼叫端配置的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                                           | Description                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**E \_ 指標**</dt> </dl>             | **Null** 指標引數。<br/>   |
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                     |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 篩選未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會將媒體類型複製到 *pType* 所指定的 **AM \_ 媒體 \_ 類型** 結構中。 呼叫端必須釋放媒體類型的格式區塊。 您可以使用 **CoTaskMemFree** 函式，或基類程式庫中的 [**FreeMediaType**](freemediatype.md) 函式。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用範例捕獲](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber 介面**](isamplegrabber.md)
</dt> </dl>

 

 




