---
description: SetMediaLength 方法會指定原始程式檔的持續時間。
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'IAMTimelineSrc：： SetMediaLength 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995484"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>IAMTimelineSrc：： SetMediaLength 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會指定原始程式檔的 `SetMediaLength` 持續時間。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*長度* 
</dt> <dd>

媒體長度，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

您可以在設定媒體停止時間之前設定媒體長度，以避免潛在的轉譯錯誤。 當您設定 media stop time 時，DES 會根據媒體長度來檢查它。

這個方法不會驗證 *長度* 參數，但值必須等於原始程式檔的實際持續時間。 藉由呼叫 [**IMediaDet：： get \_ StreamLength**](imediadet-get-streamlength.md)來取得來源檔案持續時間。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




