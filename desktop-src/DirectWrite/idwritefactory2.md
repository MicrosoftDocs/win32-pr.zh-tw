---
title: IDWriteFactory2 介面
description: 所有 DirectWrite 物件的根 factory 介面。
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- IDWriteFactory1 介面直接寫入
- IDWriteFactory1 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370292387f2c42e3f749e24a063e05bb24280ec5c8e8941a430f996fe7f349da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902798"
---
# <a name="idwritefactory2-interface"></a>IDWriteFactory2 介面

所有[DirectWrite](direct-write-portal.md)物件的根 factory 介面。

## <a name="members"></a>成員

**IDWriteFactory1** 介面繼承自 [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)。 **IDWriteFactory2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteFactory1** 介面具有這些方法。



| 方法                                                                             | 描述                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CreateCustomRenderingParams**](idwritefactory2-createcustomrenderingparams.md) | 使用指定的屬性建立呈現參數物件。<br/>                            |
| [**CreateFontFallbackBuilder**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | 建立字型 fallback builder 物件。<br/>                                                         |
| [**CreateGlyphRunAnalysis**](idwritefactory2-createglyphrunanalysis.md)           | 建立圖像執行分析物件，此物件會封裝用來呈現圖像執行的資訊。<br/> |
| [**GetSystemFontFallback**](idwritefactory2-getsystemfontfallback.md)             | 從系統字型 fallback 清單建立字型回溯物件。<br/>                              |
| [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | 在圖像執行上呼叫這個方法，以將它轉譯成多個色彩字元執行。<br/>           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

