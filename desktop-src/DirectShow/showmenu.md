---
description: 當光碟啟用或停用功能表的顯示時，就會傳送 ShowMenu 事件。
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56eb6767a8144bab3de832570db63bc4e2cdc012490f776f52b6c8977cce9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050448"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`ShowMenu`當光碟啟用或停用功能表的顯示時，就會傳送此事件。

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

指定哪些功能表已啟用或停用為數字值。



| 值 | 描述 |
|-------|-------------|
| 2     | 標題       |
| 3     | Root        |
| 4     | 子圖片  |
| 5     | 音訊       |
| 6     | 角度       |
| 7     | 章節     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

指定作業是否啟用或停用為布林值。

</dd> </dl>

 

 



