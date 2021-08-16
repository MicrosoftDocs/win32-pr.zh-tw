---
description: Windows可攜式裝置支援下列約會屬性。
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: '約會屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2ba82c12dfffb0367ab61d355d6e256ab5d97bfbeef3e4a588f3a76a5651f9b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843588"
---
# <a name="appointment-properties"></a>約會屬性

Windows可攜式裝置支援下列約會屬性。



| 屬性                                   | VarType        | 描述                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **WPD \_ 約會已 \_ 接受 \_ 出席者**  | **VT \_ LPWSTR** | 已接受約會的參與者清單（以分號分隔）。             |
| **WPD \_ 約會已 \_ 拒絕 \_ 出席者**  | **VT \_ LPWSTR** | 已拒絕約會的參與者清單（以分號分隔）。             |
| **WPD \_ 約會 \_ 位置**             | VT \_ LPWSTR     | 約會的讀取者易記位置，例如「建立5，房間7」。    |
| **WPD \_ 預約 \_ 選用 \_ 出席者**  | **VT \_ LPWSTR** | 約會的選用出席者清單（以分號分隔）。                  |
| **WPD \_ 預約 \_ 必填 \_ 出席者**  | **VT \_ LPWSTR** | 約會的必要出席者清單（以分號分隔）。                  |
| **WPD \_ 約會 \_ 資源**            | **VT \_ LPWSTR** | 約會所需資源清單（以分號分隔）。                  |
| **WPD \_ 約會 \_ 暫時 \_ 出席者** | **VT \_ LPWSTR** | 暫時接受約會的出席者清單（以分號分隔）。 |
| **WPD \_ 約會 \_ 類型**                 | **VT \_ LPWSTR** | 約會的類型，例如「個人」、「商務」等等。              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




