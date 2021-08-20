---
title: IDWriteColorGlyphRunEnumerator 介面
description: 此介面可讓應用程式透過色彩圖像執行來列舉。
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- IDWriteColorGlyphRunEnumerator 介面直接寫入
- IDWriteColorGlyphRunEnumerator 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa665f7000ffaada5bc14f97671fb6e52266c712ef6081b956184653d1f1c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536138"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>IDWriteColorGlyphRunEnumerator 介面

此介面可讓應用程式透過色彩圖像執行來列舉。 列舉值會將層級列舉為適當的圖層，以作為適當的分層。

## <a name="members"></a>成員

**IDWriteColorGlyphRunEnumerator** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDWriteColorGlyphRunEnumerator** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteColorGlyphRunEnumerator** 介面具有這些方法。



| 方法                                                                | 描述                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | 傳回列舉值目前的圖像執行。<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | 移至列舉值中的下一個圖像執行。<br/>    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

