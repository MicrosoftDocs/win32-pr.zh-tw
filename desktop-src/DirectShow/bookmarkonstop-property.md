---
description: DVDAdm. BookmarkOnStop 屬性會設定或抓取值，告知 MSWebDVD 物件是否要在使用者按一下 [停止] 按鈕時，自動儲存目前位置和設定的書簽。
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: BookmarkOnStop 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109537"
---
# <a name="bookmarkonstop-property"></a>BookmarkOnStop 屬性

`DVDAdm.BookmarkOnStop`屬性會設定或抓取值，告知 MSWebDVD 物件是否要在使用者按一下 [**停止**] 按鈕時，自動儲存目前位置和設定的書簽。

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>傳回值

傳回布林值，指出 MSDVDAdm 物件是否會儲存所有 DVD 設定的書簽，包括光碟上的位置、家長監護層和家長監護/區域。

## <a name="remarks"></a>備註

這個屬性是讀取/寫入，預設值是 false。

書簽只對特定電腦有效。 使用者無法儲存書簽，然後將它傳送給其他人，以便在不同的電腦上讀取。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



