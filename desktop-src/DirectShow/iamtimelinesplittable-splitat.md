---
description: SplitAt 方法會在指定的時間分割物件。
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'IAMTimelineSplittable：： SplitAt 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994132"
---
# <a name="iamtimelinesplittablesplitat-method"></a>IAMTimelineSplittable：： SplitAt 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SplitAt`方法會在指定的時間分割物件。

## <a name="syntax"></a>語法


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Time* 
</dt> <dd>

分割物件的時間（相對於時間軸的開始時間，以 100-毫微秒單位表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | 沒有要分割的專案。<br/>                       |
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 此物件目前不存在。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

如果您分割來源、效果或轉換，這個方法會建立相同型別的第二個物件。 原始物件會在指定的分割時間被截斷，而新的物件會取代截斷的部分。 新的物件會繼承所有相同的屬性。 在來源物件中，此方法也會分割落在分割時間的任何效果。

在追蹤上呼叫這個方法，會將追蹤中包含的所有來源、效果和轉換分割為指定的分割時間。 它不會建立第二個曲目。 (一段時間從零開始，並延伸到無限大。 ) 

針對追蹤，如果分割時間晚于追蹤中的所有專案，則此方法會傳回 \_ FALSE。 針對任何其他物件，如果分割時間不是落在物件內的任何位置，則方法會傳回 E \_ INVALIDARG。

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

[**IAMTimelineSplittable 介面**](iamtimelinesplittable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




