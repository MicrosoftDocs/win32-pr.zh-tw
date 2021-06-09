---
description: 在編解碼器中啟用低延遲模式。
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: 'CODECAPI_AVLowLatencyMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826902"
---
# <a name="codecapi_avlowlatencymode-property"></a>CODECAPI \_ AVLowLatencyMode 屬性

在編解碼器中啟用低延遲模式。

## <a name="data-type"></a>資料類型

**ULONG** (**VT \_ BOOL**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>屬性值

如果此值為非零值，則會啟用低延遲模式。 如果值為零，則會停用低延遲模式。

## <a name="remarks"></a>備註

此屬性同時適用于編碼器和解碼器。

當延遲時間應降至最低時，低延遲模式適用于即時通訊或即時捕捉。 但是，低延遲模式也可能會減少解碼或編碼品質。

編碼器預期不會因為編碼程式中的畫面格重新排列而新增任何範例延遲，而且一個輸入範例應該會產生一個輸出範例。 B 配量/框架可以存在，只要它們並未在編碼器中引進任何畫面格重新排序。

> [!WARNING] 
> 在目前的執行中，媒體基礎 h.264 解碼會針對此屬性使用類型 **VT_UI4** 。 所有其他的執行（包括 h.264 編碼器）都會使用類型 **VT_BOOL**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

