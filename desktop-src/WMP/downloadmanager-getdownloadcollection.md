---
title: DownloadManager. getDownloadCollection 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 GetDownloadCollection 方法會抓取指定的下載集合。
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- getDownloadCollection 方法 Windows Media Player
- getDownloadCollection 方法 Windows Media Player，DownloadManager 類別
- DownloadManager 類別 Windows Media Player，getDownloadCollection 方法
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000002"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>DownloadManager. getDownloadCollection 方法

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**GetDownloadCollection** 方法會抓取指定的下載集合。

## <a name="syntax"></a>語法


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*collectionId* \[在\]
</dt> <dd>

**Number** (**long**) 指定要抓取之下載集合的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **DownloadCollection** 物件。

## <a name="remarks"></a>備註

您必須先呼叫 *DownloadManager*。**createDownloadCollection** 建立新的集合，並取出其識別碼值。

現有的下載集合可能包含已標示為已取消的專案。

未在前一個會話中完成的即時下載專案，將不會被視為集合的一部分。 在目前會話之前完成的背景下載會保留在下載集合中，直到移除為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadManager 物件**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager.createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**DownloadCollection 物件**](downloadcollection-object.md)
</dt> </dl>

 

 





