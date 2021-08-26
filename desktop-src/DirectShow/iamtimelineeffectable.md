---
description: IAMTimelineEffectable 介面會提供方法，將效果新增至 DirectShow 編輯服務 (DES) 的時間軸物件，以及操作物件的效果。
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: 'IAMTimelineEffectable 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ad6b373f4b30209566709117b3b15ecf1a65d093ddb2dd27e9e0273b11ad0b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905028"
---
# <a name="iamtimelineeffectable-interface"></a>IAMTimelineEffectable 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineEffectable`介面會提供方法，將效果新增至[DirectShow 編輯服務](directshow-editing-services.md) (DES) 的時間軸物件，以及操作物件的效果。 所有可能套用效果的物件都會執行此介面;這包括來源、追蹤和組合。

執行這個介面的物件可以有任意數目的效果。 針對每個物件，轉譯引擎會依優先權順序套用其效果，從優先權層級0開始。

## <a name="members"></a>成員

**IAMTimelineEffectable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineEffectable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineEffectable** 介面具有這些方法。



| 方法                                                                     | 描述                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | 捕獲此物件的效果數目。<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | 將效果插入物件中指定的優先權層級。<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | 切換兩個效果的優先權層級。<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | 抓取指定優先權層級的效果。<br/>              |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
