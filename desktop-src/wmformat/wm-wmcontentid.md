---
title: WM/WMContentID
description: WM/WMContentID 屬性包含識別內容的 GUID。
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- WM/WMContentID windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373141"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

**WM/WMContentID** 屬性包含識別內容的 GUID。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMContentID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ GUID**

## <a name="remarks"></a>備註

使用三個值（ **wm/WMCollectionGroupID**、 **WM/WMCollectionID** 和 **WM/WMContentID**），以 Windows Media 技術來識別內容。 這些值會識別內容、其所屬的集合，以及集合所屬的群組。 當抓取內容的中繼資料時，會 Windows Media Player 填入上述三個值。 您可以讓您的應用程式記錄這些值，並使用它們來識別內容，但如果有的話，您就不應該變更它們。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




