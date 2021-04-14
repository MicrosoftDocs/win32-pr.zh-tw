---
title: WM/WMCollectionGroupID
description: WM/WMCollectionGroupID 屬性包含可識別集合群組的 GUID。
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- WM/WMCollectionGroupID windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373144"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

**WM/WMCollectionGroupID** 屬性包含可識別集合群組的 GUID。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ GUID**

## <a name="remarks"></a>備註

使用三個值（ **wm/WMCollectionGroupID**、 **WM/WMCollectionID** 和 **WM/WMContentID**），以 Windows Media 技術來識別內容。 這些值會識別內容、其所屬的集合，以及集合所屬的群組。 當抓取內容的中繼資料時，會 Windows Media Player 填入上述三個值。 您可以讓您的應用程式記錄這些值，並使用它們來識別內容，但如果有的話，您就不應該變更它們。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




