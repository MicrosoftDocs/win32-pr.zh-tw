---
description: IDxtCompositor 介面會設定組合器轉換的屬性。此介面是由 DirectShow 編輯服務在內部使用， (DES) 轉譯合成器轉換時使用。
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: 'IDxtCompositor 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984810"
---
# <a name="idxtcompositor-interface"></a>IDxtCompositor 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IDxtCompositor`介面會設定[組合](compositor-transition.md)器轉換的屬性。

此介面是由 DirectShow 編輯服務在內部使用， (DES) 轉譯合成器轉換時使用。 DES 應用程式不需要使用此介面。 若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。

組合器轉換會將前景影像合成至背景影像。 *來源矩形* 會定義以複合的前景影像區段。 *目的地矩形* 會定義接收前景影像的背景影像區段。 下圖說明這些矩形。

![組合器轉換屬性](images/compmeasure.png)

## <a name="members"></a>成員

**IDxtCompositor** 介面繼承自 **IDXEffect**。 **IDxtCompositor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDxtCompositor** 介面具有這些方法。



| 方法                                                   | 描述                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**取得 \_ 高度**](idxtcompositor-get-height.md)         | 抓取目標矩形的高度。<br/>            |
| [**取得 \_ OffsetX**](idxtcompositor-get-offsetx.md)       | 抓取目標矩形的水準位移。<br/> |
| [**取得 \_ OffsetY**](idxtcompositor-get-offsety.md)       | 抓取目標矩形的垂直位移。<br/>   |
| [**取得 \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | 抓取來源矩形的高度。<br/>            |
| [**取得 \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | 抓取來源矩形的水準位移。<br/> |
| [**取得 \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | 抓取來源矩形的垂直位移。<br/>   |
| [**取得 \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | 抓取來源矩形的寬度。<br/>             |
| [**取得 \_ 寬度**](idxtcompositor-get-width.md)           | 抓取目標矩形的寬度。<br/>             |
| [**put \_ Height**](idxtcompositor-put-height.md)         | 指定目標矩形的高度。<br/>            |
| [**put \_ OffsetX**](idxtcompositor-put-offsetx.md)       | 指定目標矩形的水準位移。<br/> |
| [**put \_ OffsetY**](idxtcompositor-put-offsety.md)       | 指定目標矩形的垂直位移。<br/>   |
| [**put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | 指定來源矩形的高度。<br/>            |
| [**put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | 指定來源矩形的水準位移。<br/> |
| [**put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | 指定來源矩形的垂直位移。<br/>   |
| [**put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | 指定來源矩形的寬度。<br/>             |
| [**put \_ 寬度**](idxtcompositor-put-width.md)           | 指定目標矩形的寬度。<br/>             |



 

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



 

 




