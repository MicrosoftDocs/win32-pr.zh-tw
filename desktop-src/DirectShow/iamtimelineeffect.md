---
description: IAMTimelineEffect 介面會提供方法，在 (DES) 的 DirectShow 編輯服務中操作音訊和影片效果。
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: 'IAMTimelineEffect 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996519"
---
# <a name="iamtimelineeffect-interface"></a>IAMTimelineEffect 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineEffect`介面提供在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中操作音訊和影片效果的方法。 效果可以加入至任何公開 [**IAMTimelineEffectable**](iamtimelineeffectable.md) 介面的時間軸物件。 若要設定效果的屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。

DES 效果物件實際上是兩個其他物件之一的包裝函式：

-   針對音訊效果，任何 DirectShow 音訊效果篩選。
-   適用于影片效果和1輸入 DirectX 轉換物件。

Microsoft 不再支援協力廠商 DirectX 轉換物件的開發。

若要指定效果的篩選或 DirectX 轉換物件，請呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法。

若要建立效果物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 與值時間軸的 \_ 主要 \_ 類型 \_ 效果。 您可以查詢傳回的介面 [**IAMTimelineObj**](iamtimelineobj.md) 指標 `IAMTimelineEffect` 。

## <a name="members"></a>成員

**IAMTimelineEffect** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineEffect** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineEffect** 介面具有這些方法。



| 方法                                                           | 描述                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | 抓取效果的優先權層級。<br/> |



 

## <a name="remarks"></a>備註

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

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
