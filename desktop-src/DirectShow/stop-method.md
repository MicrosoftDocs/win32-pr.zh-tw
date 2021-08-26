---
description: Stop 方法會停止播放。
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: '停止方法 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9eb216c3ad5c98dd1722ff941131198cfe662d025b20c3f71fe9ea758e0a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050108"
---
# <a name="stop-method-directshow"></a>停止方法 (DirectShow) 

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`Stop`方法會停止播放。

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果 [**EnableResetOnStop**](enableresetonstop-property.md) 設定為 true，則呼叫會將 DVD 導覽和 `Stop` 篩選圖形的其餘部分放入已停止的狀態，這表示當使用者下一次按下 [ **播放** ] 按鈕時，播放會從光碟開頭開始播放。如果 **EnableResetOnStop** 設為 true，當使用者發出下一個 **Play** 命令時，播放會從中斷處繼續進行。

 

 



