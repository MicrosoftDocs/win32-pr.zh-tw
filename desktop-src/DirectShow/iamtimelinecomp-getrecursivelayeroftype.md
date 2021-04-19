---
description: GetRecursiveLayerOfType 方法會針對此組合所包含的虛擬追蹤執行深度優先的排序，並從該順序抓取第 n 個虛擬追蹤。
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'IAMTimelineComp：： GetRecursiveLayerOfType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980191"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>IAMTimelineComp：： GetRecursiveLayerOfType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetRecursiveLayerOfType`方法會執行此組合中所包含之虛擬追蹤的深度優先排序，並從該順序抓取 *n* 個虛擬追蹤。

## <a name="syntax"></a>語法


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppVirtualTrack* \[擴展\]
</dt> <dd>

接收虛擬軌 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> <dt>

*WhichLayer* 
</dt> <dd>

指定要取出的虛擬追蹤（從零編制索引）。

</dd> <dt>

*型別* 
</dt> <dd>

[**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md)列舉類型的成員，指定是否要在搜尋中包含曲目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                  | Description                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 沒有指定之類型的物件。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/>       |



 

## <a name="remarks"></a>備註

一般來說，應用程式不需要呼叫這個方法。

如果 *類型* 參數是時間軸 \_ 主要 \_ 類型 \_ 追蹤，深度優先的順序就會包含追蹤。 如果沒有，則只包含組合和群組。 物件本身會包含在順序中。

例如，在下列安排中，從組合 A 開始，順序會是 B、C、F、D、E、A。

![getrecursivelayeroftype](images/composition.png)

如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

 

 




