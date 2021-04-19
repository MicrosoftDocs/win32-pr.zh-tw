---
description: IDxtJpeg 介面會設定「SMPTE 抹除」轉換的屬性。當 DirectShow 編輯服務轉譯了 SMPTE 抹除轉換時，會在內部使用此介面 (DES) 。
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: 'IDxtJpeg 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977671"
---
# <a name="idxtjpeg-interface"></a>IDxtJpeg 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IDxtJpeg`介面會設定「 [SMPTE](smpte-wipe-transition.md)抹除」轉換的屬性。

當 DirectShow 編輯服務轉譯了 SMPTE 抹除轉換時，會在內部使用此介面 (DES) 。 DES 應用程式不需要使用此介面。 若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。

## <a name="members"></a>成員

**IDxtJpeg** 介面繼承自 **IDXEffect**。 **IDxtJpeg** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDxtJpeg** 介面具有這些方法。



| 方法                                                     | 描述                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges**](idxtjpeg-applychanges.md)              | 套用已變更的任何屬性。<br/>                                      |
| [**取得 \_ 邊框**](idxtjpeg-get-bordercolor.md)       | 抓取抹除模式邊緣周圍的框線色彩。<br/>        |
| [**取得 \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | 抓取抹除模式邊緣周圍模糊區域的寬度。<br/> |
| [**取得 \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | 抓取抹除模式邊緣的實心框線寬度。<br/>   |
| [**取得 \_ MaskName**](idxtjpeg-get-maskname.md)             | 抓取要當做抹除遮罩使用的 JPEG 檔案名。<br/>                 |
| [**取得 \_ MaskNum**](idxtjpeg-get-masknum.md)               | 抓取抹除的 SMPTE 清除程式碼。<br/>                                     |
| [**取得 \_ OffsetX**](idxtjpeg-get-offsetx.md)               | 抓取抹除來源的水準位移。<br/>                            |
| [**取得 \_ OffsetY**](idxtjpeg-get-offsety.md)               | 抓取抹除來源的垂直位移。<br/>                              |
| [**取得 \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | 捕獲以水準方式複寫抹除模式的次數。<br/>     |
| [**取得 \_ ReplicateY**](idxtjpeg-get-replicatey.md)         | 捕獲以垂直方式複寫抹除模式的次數。<br/>       |
| [**取得 \_ ScaleX**](idxtjpeg-get-scalex.md)                 | 抓取抹除水準伸展的量。<br/>              |
| [**取得 \_ ScaleY**](idxtjpeg-get-scaley.md)                 | 抓取抹除垂直伸展的量。<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | 還原清除轉換的預設設定。<br/>                          |
| [**put \_ 邊框存放**](idxtjpeg-put-bordercolor.md)       | 指定抹除模式邊緣周圍的框線色彩。<br/>        |
| [**put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | 指定抹除模式邊緣周圍模糊區域的寬度。<br/> |
| [**put \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | 指定沿著抹除模式邊緣的實心框線寬度。<br/>   |
| [**put \_ MaskName**](idxtjpeg-put-maskname.md)             | 指定要用作抹除遮罩的 JPEG 檔案名。<br/>                     |
| [**put \_ MaskNum**](idxtjpeg-put-masknum.md)               | 指定抹除的 SMPTE 清除程式碼。<br/>                                     |
| [**put \_ OffsetX**](idxtjpeg-put-offsetx.md)               | 指定抹除來源的水準位移。<br/>                            |
| [**put \_ OffsetY**](idxtjpeg-put-offsety.md)               | 指定抹除來源的垂直位移。<br/>                              |
| [**put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | 指定以水準方式複寫抹除模式的次數。<br/>     |
| [**put \_ ReplicateY**](idxtjpeg-put-replicatey.md)         | 指定垂直複製抹除模式的次數。<br/>       |
| [**put \_ ScaleX**](idxtjpeg-put-scalex.md)                 | 指定以水準方式延展抹除的量。<br/>              |
| [**put \_ ScaleY**](idxtjpeg-put-scaley.md)                 | 指定抹除垂直伸展的量。<br/>                |



 

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



 

 




