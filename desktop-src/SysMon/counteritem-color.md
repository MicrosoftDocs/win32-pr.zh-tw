---
title: CounterItem。 Color 屬性
description: 抓取或設定用來繪製計數器值的色彩。
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- 色彩屬性 SysMon
- Color 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，色彩屬性
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc51862c57312f9b923ea6a80f9814182bbc6aef707dab994b135ace9637754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883865"
---
# <a name="counteritemcolor-property"></a>CounterItem。 Color 屬性

抓取或設定用來繪製計數器值的色彩。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>屬性值

用來繪製計數器值的色彩。

## <a name="remarks"></a>備註

如果您未指定要使用的色彩，SYSMON 會選取前十六個計數器的色彩。 如果您指定十六個以上的計數器，SYSMON 將會重複使用前十六個計數器的相同色彩。 為了協助區分計數器，SYSMON 會將每個16個計數器的每個倍數所使用的 [**線條樣式**](counteritem-linestyle.md) 變更為第一個80計數器。 例如，前十六個計數器使用實線樣式，接下來的十六個使用虛線樣式，依此類推。 然後 SYSMON 會將計數器 81-96 的 [**線條寬度**](counteritem-width.md) 設定為2，並將計數器 96-112 設定為3。 如果集合包含112個以上的計數器，計數器將會包含重複的色彩、線條樣式和寬度值。

**在 Windows Vista 之前：** 如果您未指定要使用的色彩，SYSMON 會選取前十六個計數器的色彩。 如果您指定十六個以上的計數器，SYSMON 將會重複使用前十六個計數器的相同色彩。 為了協助區分計數器，SYSMON 會增加接收相同色彩指派之前三個計數器的 [**行寬**](counteritem-width.md) 。 如果有三個以上的計數器使用相同的色彩，SYSMON 會隨機播放要用於計數器的線條寬度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





