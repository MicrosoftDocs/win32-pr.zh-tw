---
title: IDWriteLocalFontFileLoader 介面
description: IDWriteFontFileLoader 介面的內建執行，可在本機字型檔案上運作，並公開字型檔案參考索引鍵的本機字型檔案資訊。
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- IDWriteLocalFontFileLoader 介面直接寫入
- IDWriteLocalFontFileLoader 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa073b0d39e5dfbcdb90f2cd67db5f09a04e21c3e36790d4d841e5719490c753
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048688"
---
# <a name="idwritelocalfontfileloader-interface"></a>IDWriteLocalFontFileLoader 介面

[**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)介面的內建執行，可在本機字型檔案上運作，並公開字型檔案參考索引鍵的本機字型檔案資訊。 使用 [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 建立的字型檔案參考會使用這個字型檔案載入器。

## <a name="members"></a>成員

**IDWriteLocalFontFileLoader** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDWriteLocalFontFileLoader** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteLocalFontFileLoader** 介面具有這些方法。



| 方法                                                                                  | 描述                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | 從字型檔案參考索引鍵取得絕對字型檔案路徑。<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | 從字型檔案參考索引鍵取得絕對檔案路徑的長度。<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | 從字型檔案參考索引鍵取得檔案的上次寫入時間。<br/>      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Dwrite .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

