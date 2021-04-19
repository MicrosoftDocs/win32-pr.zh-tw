---
description: SetOutputBuffering 方法會指定預覽期間預先轉譯的畫面格數目。
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'IAMTimelineGroup：： SetOutputBuffering 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999468"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>IAMTimelineGroup：： SetOutputBuffering 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetOutputBuffering`方法會指定預覽期間預先轉譯的畫面格數。

## <a name="syntax"></a>語法


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nBuffer* \[在\]
</dt> <dd>

預覽期間要緩衝的框架數目。 必須是2或以上。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

較大的緩衝區需要更多記憶體，但會導致更流暢的預覽，尤其是在需要更多時間轉譯的效果或轉換期間。 預設緩衝區為30個畫面格。

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

[**IAMTimelineGroup 介面**](iamtimelinegroup.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




