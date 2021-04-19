---
title: DownloadItem. getItemInfo 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 GetItemInfo 方法會抓取下載專案的屬性值。
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，DownloadItem 類別
- DownloadItem 類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992860"
---
# <a name="downloaditemgetiteminfo-method"></a>DownloadItem. getItemInfo 方法

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**GetItemInfo** 方法會抓取下載專案的屬性值。

## <a name="syntax"></a>語法


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>參數

<dl> <dt>

的是 \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。 支援的值為 AlbumArtist、專輯、Duration、WM/Provider、Title、UserRating 和 WM/TrackNumber。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** ，其中 *包含依元素* 指定的屬性值。

## <a name="remarks"></a>備註

這個方法會使用 BITS 描述字串來抓取指定的屬性。 請參閱 [WINDOWS MEDIA PLAYER BITS 作業慣例](windows-media-player-bits-job-convention.md)。

此方法支援背景下載。 使用即時下載時，您的程式碼不應呼叫這個方法。

這個方法可以取得目前 Windows Media Player 會話期間所新增之 BITS 工作的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadItem。類型**](downloaditem-type.md)
</dt> <dt>

[**DownloadItem 物件**](downloaditem-object.md)
</dt> </dl>

 

 





