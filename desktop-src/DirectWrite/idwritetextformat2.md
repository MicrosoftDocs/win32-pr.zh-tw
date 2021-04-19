---
title: IDWriteTextFormat2 介面
description: 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。 |IDWriteTextFormat2 介面
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- IDWriteTextFormat2 介面直接寫入
- IDWriteTextFormat2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992269"
---
# <a name="idwritetextformat2-interface"></a>IDWriteTextFormat2 介面

描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。

## <a name="members"></a>成員

**IDWriteTextFormat2** 介面繼承自 [**IDWriteTextFormat1**](idwritetextformat1.md)。 **IDWriteTextFormat2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteTextFormat2** 介面具有這些方法。



| 方法                                                      | 描述                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetLineSpacing**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | 取得多行文欄位落的行間距調整集。 <br/> |
| [**SetLineSpacing**](idwritetextformat2-setlinespacing.md) | 設定行間距。<br/>                                                     |



 

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

[**IDWriteTextFormat1**](idwritetextformat1.md)
</dt> </dl>

 

