---
description: VTrackInsBefore 方法會依指定的優先順序，將虛擬追蹤插入組合中。
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'IAMTimelineComp：： VTrackInsBefore 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996455"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>IAMTimelineComp：： VTrackInsBefore 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會依 `VTrackInsBefore` 指定的優先順序，將虛擬追蹤插入組合中。

## <a name="syntax"></a>語法


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

虛擬追蹤的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。

</dd> <dt>

*優先順序* 
</dt> <dd>

要插入虛擬追蹤的優先順序，或-1 則會在優先順序清單的結尾插入虛擬記錄。 優先權清單決定哪些剪輯是可見的。 如需詳細資訊，請參閱「備註」。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                   | Description                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效引數。<br/>              |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | 物件不是虛擬追蹤。<br/> |



 

## <a name="remarks"></a>備註

組合中的每個虛擬追蹤都有唯一的優先權層級。 優先權層級的範圍是從0到 *n* -1，其中 *n* 是組合中的虛擬追蹤數目。 若為影片群組，虛擬追蹤會以較低的優先權層級隱藏任何虛擬追蹤，但追蹤是空的或包含轉換的位置除外。 您可以將虛擬追蹤視為最終組合中的圖層。 Track 1 會分層置於曲目0的上方，而 track 2 則會分層顯示在曲目1的上方，依此類推。

如果您為 *Priority* 參數指定-1，則會在清單結尾插入虛擬追蹤，而且優先順序值會高於現有的追蹤。 如果您指定的優先順序值已存在於組合中，則每個具有相等或更高優先順序的追蹤都會向上移動一個優先權層級。

**範例**：追蹤 A 具有優先權0，而追蹤 B 的優先順序為1。 如果在優先順序0插入追蹤 C，請追蹤移至優先順序1，並將追蹤 B 移至優先順序2。

如果指定的優先順序大於組合中目前的曲目數，則方法會失敗。

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

[**IAMTimelineComp 介面**](iamtimelinecomp.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




