---
title: DownloadManager
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 DownloadManager 屬性會捕獲 DownloadManager 物件。
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- DownloadManager Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d828435c43f57406e637312245b2bb3ae3e7c35510c9b2daf478a7fec39b599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649208"
---
# <a name="externaldownloadmanager"></a>DownloadManager

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**DownloadManager** 屬性會捕獲 **DownloadManager** 物件。

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **DownloadManager** 物件。

## <a name="remarks"></a>備註

在 Windows Media Player 10 或更新版本中， **DownloadManager** 屬性和物件只能從 [線上商店服務] 工作窗格存取。 您無法使用 **外部** 物件可用之其他功能的 **DownloadManager** ，例如 HTMLView、資訊中心視圖和專輯資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型2線上商店的外部物件**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





