---
description: IAMTimelineTrans 介面提供在 DirectShow 編輯服務 (DES) 中操作轉換的方法。
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: 'IAMTimelineTrans 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28d7fd409c3ab377393f6c70359d0f6a0a07a3e14c64a77acb2912d9863c6d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998721"
---
# <a name="iamtimelinetrans-interface"></a>IAMTimelineTrans 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineTrans`介面提供在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中操作轉換的方法。 轉換是指一個影片圖層和以較低優先順序呈現的所有影片層級之間的進展。 轉換可以新增至任何可公開 [**IAMTimelineTransable**](iamtimelinetransable.md) 介面的時間軸物件。 若要設定轉換的屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。

DES 轉換物件實際上是 DirectX 轉換物件的包裝函式。 任何2輸入的 DirectX 轉換物件都可以用來執行轉換的視覺效果。 Microsoft 不再支援協力廠商 DirectX 轉換物件的開發。 若要指定轉換的 DirectX 轉換物件，請呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法。

若要建立轉換物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) ，其值時間軸 \_ 主要 \_ 類型 \_ 轉換。 您可以查詢傳回的介面 [**IAMTimelineObj**](iamtimelineobj.md) 指標 `IAMTimelineTrans` 。

## <a name="members"></a>成員

**IAMTimelineTrans** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineTrans** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineTrans** 介面具有這些方法。



| 方法                                                  | 描述                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GetCutPoint**](iamtimelinetrans-getcutpoint.md)     | 抓取剪下點。<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | 以 [**REFTIME**](reftime.md) 值形式捕獲剪下點。<br/>             |
| [**GetCutsOnly**](iamtimelinetrans-getcutsonly.md)     | 判斷轉換是否轉譯為剪下。<br/>                     |
| [**GetSwapInputs**](iamtimelinetrans-getswapinputs.md) | 抓取值，這個值表示是否交換轉換輸入。<br/> |
| [**SetCutPoint**](iamtimelinetrans-setcutpoint.md)     | 設定剪下點。<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | 將剪點設定為 [**REFTIME**](reftime.md) 值。<br/>                  |
| [**SetCutsOnly**](iamtimelinetrans-setcutsonly.md)     | 指定轉換是否轉譯為剪下。<br/>                      |
| [**SetSwapInputs**](iamtimelinetrans-setswapinputs.md) | 指定是否交換轉換輸入。<br/>                        |



 

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
