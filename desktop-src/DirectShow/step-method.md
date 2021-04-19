---
description: Step 方法會將 DVD-Video 資料流程前移至指定的框架數。
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984656"
---
# <a name="step-method"></a>Step 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會將 `Step` DVD-Video 資料流程前移至指定的框架數。

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframe*
</dt> <dd>

指定要逐步執行為整數的框架數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**CanStep**](canstep-method.md) 來判斷此解碼器是否支援框架逐步執行。

如果在呼叫這個方法時，DVD-Video 在反向模式下播放，而且此解碼器支援反向框架逐步執行，則會反向執行框架逐步執行。

 

 



