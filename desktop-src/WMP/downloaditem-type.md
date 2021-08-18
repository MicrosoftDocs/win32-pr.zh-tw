---
title: DownloadItem。類型
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Type 屬性會抓取下載的型別。
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem 輸入 Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038f348093a512095ee930c4147024bc789ead5edd3498243eb83a01608bfac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749709"
---
# <a name="downloaditemtype"></a>DownloadItem。類型

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Type** 屬性會抓取下載的型別。

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串** ，其中包含下列其中一個值。



| 值      | 描述                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 背景資訊 |  (Windows XP。 ) 下載會在處理器時間變成可用時，做為背景進程。 即使在 Windows Media Player 或 Windows XP 關閉時，下載狀態仍然存在。 |
| 即時  |  (所有支援的作業系統。 ) 下載會一次完成。 會話之間不會保存任何下載狀態。                                                                       |



 

## <a name="remarks"></a>備註

每種類型的下載都有其優點和缺點。 背景下載可讓使用者繼續進行其他工作，甚至重新開機 Windows 而不需要取消下載，但需要更多時間才能完成下載，且僅支援 Windows XP。 即時下載需要較少的時間才能完成，但會要求使用者在關閉 Windows Media Player 之前完成下載。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadItem 物件**](downloaditem-object.md)
</dt> </dl>

 

 





