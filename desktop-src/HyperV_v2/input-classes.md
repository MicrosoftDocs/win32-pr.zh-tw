---
description: 使用者輸入裝置是由這些類別表示。 虛擬機器一律會有一個與其相關聯之類別的實例。
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: 輸入類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979052"
---
# <a name="input-classes"></a>輸入類別

使用者輸入裝置是由這些類別表示。 虛擬機器一律會有一個與其相關聯之類別的實例。 這些裝置可能不會在虛擬機器中新增或移除。 因此，鍵盤或滑鼠裝置沒有資源集區實例。

鍵盤和滑鼠裝置會透過 [**Msvm \_ SystemDevice**](msvm-systemdevice.md) 關聯連結到虛擬機器。 虛擬機器包含 PS2 和綜合滑鼠裝置。 一次只能有一個作用中的指向裝置。

以下是與輸入相關的虛擬化 WMI 類別。

## <a name="in-this-section"></a>本節內容



| 主題                                                          | 描述                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**Msvm \_ 鍵盤**](msvm-keyboard.md)<br/>             | 代表鍵盤裝置。<br/>        |
| [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | 表示 PS2 滑鼠裝置。<br/>       |
| [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | 代表綜合滑鼠裝置。<br/> |



 

 

 




