---
description: 存取 DirectDraw 表面
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: 存取 DirectDraw 表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff443550cb6a922a3361b6d75b880eb427edf79e3a3232c21ab6aad0c06ec483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873568"
---
# <a name="access-to-directdraw-surfaces"></a>存取 DirectDraw 表面

VMR 提供給上游篩選器的媒體範例物件支援 [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) 介面。 若要取得介面，請呼叫 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面上的 QueryInterface 並指定 IID \_ IVMRSurface。 上游篩選器接著可以使用 IVMRSurface 方法來存取及操作由 VMR 所建立的介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[針對 DirectShow 濾波器開發人員使用 VMR](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



