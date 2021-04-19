---
description: SetDefaultFPS 方法會設定來源物件的預設畫面播放速率。
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'IAMTimelineSrc：： SetDefaultFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983113"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>IAMTimelineSrc：： SetDefaultFPS 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetDefaultFPS`方法會設定來源物件的預設畫面播放速率。

## <a name="syntax"></a>語法


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FPS* 
</dt> <dd>

預設畫面播放速率（以每秒畫面格速率為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK， \_ 如果指定的畫面播放速率小於零，則傳回 E INVALIDARG。

## <a name="remarks"></a>備註

如果轉譯引擎無法從原始來源檔案判斷畫面播放速率，則會使用此值。

請僅針對原始程式檔呼叫這個方法，而不使用預先定義的畫面播放速率。 若是點陣圖和 JPEG 檔案，預設畫面播放速率是零，這會導致來源轉譯為靜止影像。 若要使用影像做為 DIB 順序中的第一個畫面格，請將畫面播放速率設定為大於零的值。 如需詳細資訊，請參閱 [使用來源](working-with-sources.md)。

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

 

 




