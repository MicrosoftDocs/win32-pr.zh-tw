---
description: DVDAdm. DefaultSubpictureLCID 屬性會針對使用者指定的子圖片資料流程預設 LCID 設定或抓取登錄設定。
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: DefaultSubpictureLCID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510357"
---
# <a name="defaultsubpicturelcid-property"></a>DefaultSubpictureLCID 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會針對 `DVDAdm.DefaultSubpictureLCID` 使用者指定的子圖片資料流程預設 LCID 設定或抓取登錄設定。

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>傳回值

傳回整數值，代表使用者指定的預設子圖片 LCID （儲存在 DVD 應用程式的登錄設定中）。 此值不一定與 DVD 上所撰寫的預設子圖片資料流程相同。 如需有效的 Lcid 範圍，請參閱 Platform SDK 中的 Win32 檔。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，沒有預設值。 如果未指定預設子圖片 LCID，MSDVDAdm 物件將會播放標示為光碟上預設資料流程的子圖片串流。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



