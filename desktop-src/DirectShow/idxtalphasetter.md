---
description: IDxtAlphaSetter 介面會設定 Alpha Setter 效果的屬性。當 DirectShow 編輯服務轉譯 Alpha Setter 效果時，會在內部使用此介面 (DES) 。
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: 'IDxtAlphaSetter 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985779"
---
# <a name="idxtalphasetter-interface"></a>IDxtAlphaSetter 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IDxtAlphaSetter`介面會設定[Alpha Setter](alpha-setter-effect.md)效果上的屬性。

當 DirectShow 編輯服務轉譯 Alpha Setter 效果時，會在內部使用此介面 (DES) 。 DES 應用程式不需要使用此介面。 若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。

## <a name="members"></a>成員

**IDxtAlphaSetter** 介面繼承自 **IDXEffect**。 **IDxtAlphaSetter** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDxtAlphaSetter** 介面具有這些方法。



| 方法                                                  | 描述                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**取得 \_ Alpha**](idxtalphasetter-get-alpha.md)         | 抓取整個影像的 Alpha 值。<br/> |
| [**取得 \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | 抓取 Alpha 曲線的屬性。<br/>              |
| [**put \_ Alpha**](idxtalphasetter-put-alpha.md)         | 指定整個影像的 Alpha 值。<br/> |
| [**put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | 指定 Alpha 曲線的屬性。<br/>              |



 

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



 

 




