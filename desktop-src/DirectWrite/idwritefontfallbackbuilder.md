---
title: IDWriteFontFallbackBuilder 介面
description: 可讓您建立 Unicode 字型回撥對應，並從這些對應中建立字型的物件。
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- IDWriteFontFallbackBuilder 介面直接寫入
- IDWriteFontFallbackBuilder 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934612"
---
# <a name="idwritefontfallbackbuilder-interface"></a>IDWriteFontFallbackBuilder 介面

可讓您建立 Unicode 字型回撥對應，並從這些對應中建立字型的物件。

## <a name="members"></a>成員

**IDWriteFontFallbackBuilder** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDWriteFontFallbackBuilder** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteFontFallbackBuilder** 介面具有這些方法。



| 方法                                                                      | 描述                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | 將單一對應附加至清單。 針對每個額外的對應呼叫一次。<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | 從現有的字型回溯物件加入所有對應。<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | 從新增的對應建立已完成的 fallback 物件。<br/>                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

