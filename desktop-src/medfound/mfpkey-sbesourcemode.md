---
description: 設定 WTV 媒體來源的資料流程設定。
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: 'MFPKEY_SBESourceMode 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c6b4fc0b248000f0540fd47fd7bbf8bba907994d1351144521bf162d330340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973367"
---
# <a name="mfpkey_sbesourcemode-property"></a>MFPKEY \_ SBESourceMode 屬性

設定 WTV 媒體來源的資料流程設定。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**INT**

VT \_ INT

**intVal**



## <a name="remarks"></a>備註

使用此屬性可設定 WTV 媒體來源。 若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

WTV 媒體來源會讀取 Windows 錄製的電視節目 (. WTV 和 winspool.drv) 檔。

這個屬性必須具有下列其中一個值。

-   1：根據系統本機，將可用的音訊串流對應至單一輸出。 此模式適用于播放。 (預設值。)
-   2. 系統會選取所有音訊串流和子串流 (例如標題和資料流程) 。 此模式適用于 remuxing 或轉碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
