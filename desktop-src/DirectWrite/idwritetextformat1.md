---
title: IDWriteTextFormat1 介面
description: 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。 |IDWriteTextFormat1 介面
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- IDWriteTextFormat1 介面直接寫入
- IDWriteTextFormat1 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106979861"
---
# <a name="idwritetextformat1-interface"></a>IDWriteTextFormat1 介面

描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。 這個介面具有與 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 相同的所有方法，並新增了套用明確方向的能力。

## <a name="members"></a>成員

**IDWriteTextFormat1** 介面繼承自 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)。 **IDWriteTextFormat1** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteTextFormat1** 介面具有這些方法。



| 方法                                                                                | 描述                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | 取得目前的回退。 如果建立配置之後未曾設定任何內容，則會是 nullptr。<br/>               |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | 取得最後一行的包裝模式。<br/>                                                                     |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | 取得文字格式的光學邊界對齊。<br/>                                                       |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | 使用垂直閱讀方向時，取得字型的慣用方向。<br/>                             |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | 將自訂字型回套用至版面配置。 如果未設定任何值，則會使用預設的系統 fallback 清單。 <br/> |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | 設定最後一行的包裝模式。<br/>                                                                     |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | 設定文字格式的光學邊界對齊。<br/>                                                       |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | 設定文字格式的方向。<br/>                                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

