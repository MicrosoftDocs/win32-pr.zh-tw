---
description: Step 方法會將 DVD-Video 資料流程前移至指定的框架數。
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5738e8704b24d64a429d8d38f1b9eac2f9b8ff7e22a7e9d1d2a29fb9df4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050308"
---
# <a name="step-method"></a>Step 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

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

 

 



