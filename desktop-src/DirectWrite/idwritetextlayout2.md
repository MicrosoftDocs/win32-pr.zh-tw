---
title: IDWriteTextLayout2 介面
description: 表示經過完整分析和格式化之後的一段文字。 |IDWriteTextLayout2 介面
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- IDWriteTextLayout2 介面直接寫入
- IDWriteTextLayout2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff23fea3d1ae4da7c6dba310ed28dfb8c76d65947426f0219e3868f3859c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816258"
---
# <a name="idwritetextlayout2-interface"></a>IDWriteTextLayout2 介面

表示經過完整分析和格式化之後的一段文字。

## <a name="members"></a>成員

**IDWriteTextLayout2** 介面繼承自 [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)。 **IDWriteTextLayout2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteTextLayout2** 介面具有這些方法。



| 方法                                                                                | 描述                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | 取得目前的字型 fallback 物件。 <br/>                                           |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | 取得最後一行中的最後一個單字是否換行。<br/>                    |
| [**GetMetrics**](idwritetextlayout2-getmetrics.md)                                   | 抓取格式化字串的整體計量。 <br/>                             |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | 取得字元與邊界邊緣的對齊方式。 <br/>                               |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | 使用垂直閱讀方向時，取得字型的慣用方向。<br/> |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | 將自訂字型回套用至版面配置。<br/>                                        |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | 設定是否要包裝最後一行的最後一個字組。 <br/>                   |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | 設定字型與邊界邊緣的對齊方式。<br/>                                |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | 使用垂直閱讀方向時，請設定字型的慣用方向。<br/> |



 

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

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

