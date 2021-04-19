---
description: GetPreviewMode 方法會抓取群組的預覽模式。
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'IAMTimelineGroup：： GetPreviewMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991254"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a>IAMTimelineGroup：： GetPreviewMode 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetPreviewMode` 群組的預覽模式。

## <a name="syntax"></a>語法


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfPreview* 
</dt> <dd>

接收指出預覽模式的布林值。 若 **為 TRUE**，則群組處於預覽模式。 如果 **為 FALSE**，則表示群組處於撰寫模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

在預覽模式中，會在慢速效果或轉換期間卸載框架，讓影片與音訊保持同步。 這樣的影片看起來可能不穩定。 在 [撰寫中] 模式中，每個畫面格都會呈現。 撰寫模式適合用來寫入檔案;在螢幕上預覽時，影片可能會與音訊不同步。

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

 

 




