---
description: DVDAdm. DefaultMenuLCID 屬性會設定或抓取使用者為功能表指定之預設 LCID 的登錄設定。
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: DefaultMenuLCID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 939f65ad41cb184f38e2a30392030ca67066fe203f7952441cc2f77b1db95242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906888"
---
# <a name="defaultmenulcid-property"></a>DefaultMenuLCID 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.DefaultMenuLCID`屬性會設定或抓取使用者為功能表指定之預設 LCID 的登錄設定。

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>傳回值

傳回整數值，代表儲存在 DVD 應用程式之登錄設定中的 LCID。 此值與在 DVD 上撰寫的預設功能表語言不一定相同。 如需有效的 Lcid 範圍，請參閱 Platform SDK 中的 Win32 檔。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，沒有預設值。 如果未指定預設的功能表 LCID，MSDVDAdm 物件會使用標示為光碟上預設功能表語言的語言。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



