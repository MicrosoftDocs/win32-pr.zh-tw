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
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083862"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

**WM/WMContentID** 屬性包含識別內容的 GUID。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMContentID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ GUID**

## <a name="remarks"></a>備註

內容是藉由使用三個值 Windows 媒體技術來識別： **WM/WMCollectionGroupID**、 **WM/WMCollectionID** 和 **WM/WMContentID**。 這些值會識別內容、其所屬的集合，以及集合所屬的群組。 當抓取內容的中繼資料時，會 Windows Media Player 填入上述三個值。 您可以讓您的應用程式記錄這些值，並使用它們來識別內容，但如果有的話，您就不應該變更它們。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




