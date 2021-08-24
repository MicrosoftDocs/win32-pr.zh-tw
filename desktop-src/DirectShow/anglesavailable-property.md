---
description: AnglesAvailable 屬性會抓取目前可用的角度數目。
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: AnglesAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071b70fc5a5a3bc7569474d6628a92c3b7fca0138c5bbbd5780cc1e9f6be8882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001468"
---
# <a name="anglesavailable-property"></a>AnglesAvailable 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `AnglesAvailable` 目前可用的角度數目。

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>傳回值

傳回從1到9的整數值，代表目前可用的角度數目。 如果


```
iAngles
```



= 1，目前位置沒有角區塊。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 *角度區塊* 是從一個以上相機角度拍攝的影片區段。 角度區塊中最多可以有九個角度，從1到9的編號。 當 DVD 導覽器第一次進入角度區塊時，會以 \_ lParam1 中的角度數，將 EC DVD \_ 角度 \_ 可用事件通知傳送給您的應用程式。 您可以撰寫光碟來自動顯示可用角度的功能表（當其進入角度區塊時），但通常應用程式必須判斷可用的角度，並提供使用者一種方式來選取它。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CurrentAngle**](currentangle-property.md)
</dt> </dl>

 

 



