---
description: 包含應用程式 IMFSourceOpenMonitor 介面的指標。
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: 'MFPKEY_SourceOpenMonitor 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45594e1929e66982d3e518c4ba098d2ca4b22e854e033dc69025aaf3ec5d5cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872984"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>MFPKEY \_ SourceOpenMonitor 屬性

包含應用程式之 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面的指標。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**IUnknown** 指標

VT \_ 不明

**punkVal**



## <a name="remarks"></a>備註

應用程式可以將此屬性傳遞至來源解析程式，以從網路來源取得事件通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




