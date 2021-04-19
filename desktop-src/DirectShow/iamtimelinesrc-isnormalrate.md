---
description: IsNormalRate 方法會指出剪輯是否會以正常播放速率播放;也就是原始檔案的播放速度。
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'IAMTimelineSrc：： IsNormalRate 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993541"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>IAMTimelineSrc：： IsNormalRate 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IsNormalRate`方法會指出剪輯是否會以正常播放速率播放，也就是原始檔案的播放速度。

## <a name="syntax"></a>語法


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* 
</dt> <dd>

接收布林值，指出剪輯將如何轉譯。 如果該值為 **TRUE**，則會以一般速率播放剪輯。 否則，它的播放速度會比平常更快或更慢。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

剪輯的播放速率取決於其媒體的開始和停止時間，相對於其時間軸時間：


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



如果此比率等於1，則剪輯會以撰寫的速度播放。 否則，它的播放速度會更快或更慢。 如需詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。

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

 

 




