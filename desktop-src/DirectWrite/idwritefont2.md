---
title: IDWriteFont2 介面
description: 代表字型集合中的實體字型。
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- IDWriteFont2 介面直接寫入
- IDWriteFont2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5956c14a203020106fe6ecafdffb1522810d8f56684bbeafd158045444e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071683"
---
# <a name="idwritefont2-interface"></a>IDWriteFont2 介面

代表字型集合中的實體字型。

這個介面會新增檢查色彩轉譯路徑是否可能需要的功能。

## <a name="members"></a>成員

**IDWriteFont2** 介面繼承自 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)。 **IDWriteFont2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDWriteFont2** 介面具有這些方法。



| 方法                                          | 描述                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**IsColorFont**](idwritefont2-iscolorfont.md) | 可判斷是否有可能需要色彩轉譯路徑。<br/> |



 

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

[**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

