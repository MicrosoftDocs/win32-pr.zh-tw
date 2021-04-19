---
title: DownloadItem.downloadState
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 DownloadState 屬性會捕獲下載的狀態。
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadState Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997749"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem.downloadState

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**DownloadState** 屬性會捕獲下載的狀態。

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** ，其中包含下列其中一個值。



| 值 | 描述 |
|-------|-------------|
| 0     | 正在下載 |
| 1     | 已暫停      |
| 2     | Processing  |
| 3     | 已完成   |
| 4     | 已取消    |



 

## <a name="remarks"></a>備註

下載狀態可能會以任何順序發生。 請勿撰寫相依于任何特定下載狀態之出現位置的程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadItem 物件**](downloaditem-object.md)
</dt> </dl>

 

 





