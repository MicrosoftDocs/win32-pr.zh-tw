---
description: DVDAdm BookmarkOnClose 屬性會設定或抓取值，告知 MSDVDAdm 物件是否要在使用者關閉應用程式時，自動儲存目前位置和設定的書簽。
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: BookmarkOnClose 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317747"
---
# <a name="bookmarkonclose-property"></a>BookmarkOnClose 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.BookmarkOnClose`屬性會設定或抓取值，告知 MSDVDAdm 物件是否要在使用者關閉應用程式時，自動儲存目前位置和設定的書簽。

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>傳回值

傳回布林值，如果為 true，表示 MSDVDAdm 控制項將會儲存所有 DVD 設定的書簽，包括光碟上的位置、家長監護，以及當使用者關閉 DVD 播放機應用程式時的家長監護/區域。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，預設值為 true。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



