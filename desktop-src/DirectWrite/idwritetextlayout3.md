---
title: IDWriteTextLayout3 介面
description: 表示經過完整分析和格式化之後的一段文字。 |IDWriteTextLayout3 介面
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- IDWriteTextLayout3 介面直接寫入
- IDWriteTextLayout3 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f3a6d441c3f7d8ac9bf356bd835f800e026f8c6e27cb083a57ced571ba68fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070648"
---
# <a name="idwritetextlayout3-interface"></a>IDWriteTextLayout3 介面

表示經過完整分析和格式化之後的一段文字。

## <a name="members"></a>成員

**IDWriteTextLayout3** 介面繼承自 [**IDWriteTextLayout2**](idwritetextlayout2.md)。 **IDWriteTextLayout3** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteTextLayout3** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | 抓取每一行的屬性。<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | 取得行距資訊。<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | 使版面配置失效，並在呼叫度量或繪圖函式之前強制重新測量配置。 如果字型的位置變更、配置應重新繪製，或如果用戶端的大小已實 IDWriteInlineObject 變更，這項功能就很有用。 <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | 設定行間距。<br/>                                                                                                                                                                                                                                         |



 

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

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





