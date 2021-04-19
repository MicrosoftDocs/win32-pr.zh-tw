---
description: ReadyState 屬性會捕獲 MSWebDVD 物件的 ReadyState。
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: 'ReadyState 屬性 (Ocidl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989562"
---
# <a name="readystate-property"></a>ReadyState 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`ReadyState`屬性會捕獲 **MSWebDVD** 物件的 ReadyState。

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>傳回值

傳回整數值，代表控制項的 ReadyState。



| 傳回碼 | 描述                                               |
|-------------|-----------------------------------------------------------|
| 0           | 預設初始化狀態。                             |
| 1           | 物件正在載入其屬性。                         |
| 2           | 物件已初始化。                              |
| 3           | 物件是互動式的，但並非所有的資料都可供使用。 |
| 4           | 物件已接收其所有資料。                         |



 

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。

內嵌在網頁中的任何物件都會公開 `ReadyState` 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ocidl。h</dt> </dl> |



 

 




