---
description: SubpictureStreamsAvailable 屬性會抓取目前標題中可用的子圖片資料流程數目。
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: SubpictureStreamsAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978145"
---
# <a name="subpicturestreamsavailable-property"></a>SubpictureStreamsAvailable 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `SubpictureStreamsAvailable` 目前標題中可用的子圖片資料流程數目。

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>傳回值

以整數形式傳回可用資料流程的數目。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 若要查詢每個資料流程的語言屬性，請先呼叫這個方法來取得上限。

資料流程編號以零為基底。

 

 



