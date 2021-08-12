---
title: D1102 太多開啟的控制碼
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: 找到大量的未發行介面。 目前此 DLL 配置了未發行介面。
keywords:
- D1102 太多開啟的控制碼 Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: baaa4c46850919aed50897583bfa68c9003bcf496ad884c68cfb57d3e8a90147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666349"
---
# <a name="d1102-too-many-opened-handles"></a>D1102：太多開啟的控制碼

找到大量的未發行介面。 目前此 DLL 配置了 \[ *數目* 的 \] 未發行介面。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*數量*
</dt> <dd>

由此 DLL 配置的未發行介面數目。

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| 錯誤層級 | 警告 |



 

## <a name="possible-causes"></a>可能的原因

已建立大量的資源。 雖然 Direct2D 的可用資源數量沒有上限 (但記憶體) 除外，但在遇到1001的即時物件、2001即時物件或3001的即時物件等時，debug 層會發出這項參考用訊息，因為這可能表示應用程式中發生流失。

 

 




