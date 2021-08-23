---
description: DVDAdm. DefaultAudioLCID 屬性會設定或抓取使用者指定之音訊資料流程預設 LCID 的登錄設定。
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: DefaultAudioLCID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7ebcd864f8ac3bff8cfd8556703dd091985a72c0dfea4f0eefb9f974213165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953002"
---
# <a name="defaultaudiolcid-property"></a>DefaultAudioLCID 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.DefaultAudioLCID`屬性會設定或抓取使用者指定之音訊資料流程預設 LCID 的登錄設定。

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>傳回值

傳回整數值，表示儲存在 DVD 應用程式之登錄設定中的使用者指定預設音訊 LCID。 此值不一定與 DVD 上所撰寫的預設音訊資料流程相同。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，沒有預設值。 如果未指定預設音訊 LCID，MSDVDAdm 物件將會播放標示為光碟上預設資料流程的音訊串流。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



