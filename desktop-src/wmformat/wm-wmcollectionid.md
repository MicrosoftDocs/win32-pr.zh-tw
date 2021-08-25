---
title: WM/WMCollectionID
description: WM/WMCollectionID 屬性包含可識別集合的 GUID。
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- WM/WMCollectionID windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928828"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

**WM/WMCollectionID** 屬性包含可識別集合的 GUID。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMCollectionID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ GUID**

## <a name="remarks"></a>備註

內容是藉由使用三個值 Windows 媒體技術來識別： **WM/WMCollectionGroupID**、 **WM/WMCollectionID** 和 **WM/WMContentID**。 這些值會識別內容、其所屬的集合，以及集合所屬的群組。 當抓取內容的中繼資料時，會 Windows Media Player 填入上述三個值。 您可以讓您的應用程式記錄這些值，並使用它們來識別內容，但如果有的話，您就不應該變更它們。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




