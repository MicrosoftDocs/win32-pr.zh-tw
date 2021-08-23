---
title: OpenState
description: OpenState 屬性會抓取值，指出內容來源的狀態。
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- OpenState Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c0b88d3cab5d5bae4efb1e9a2a5032709943d82484b073302bf0b45a6f5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995978"
---
# <a name="playeropenstate"></a>OpenState

**OpenState** 屬性會抓取值，指出內容來源的狀態。

## <a name="syntax"></a>Syntax

*玩家* 。**openState**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。 C 樣式的列舉常數可以藉由在 state 值前面加上 "wmpos" 來衍生。 例如，PlaylistOpening 狀態的常數為 **wmposPlaylistOpening**。



| 值 | 州                   | 描述                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 未定義               | Windows Media Player 處於未定義狀態。                                                                                                         |
| 1     | PlaylistChanging        | 即將載入新的播放清單。                                                                                                                    |
| 2     | PlaylistLocating        | Windows Media Player 正在嘗試找出播放清單。 播放清單可以是本機 (程式庫，或副檔名為 .asx 的中繼檔) 或遠端。 |
| 3     | PlaylistConnecting      | 連接到播放清單。                                                                                                                            |
| 4     | PlaylistLoading         | 已找到播放清單，現在正在進行取出。                                                                                                    |
| 5     | PlaylistOpening         | 播放清單已被取出，現在正在進行剖析和載入。                                                                                        |
| 6     | PlaylistOpenNoMedia     | 播放清單已開啟。                                                                                                                                      |
| 7     | PlaylistChanged         | 已將新的播放清單指派給 **currentPlaylist**。                                                                                               |
| 8     | MediaChanging           | 即將載入新的媒體專案。                                                                                                                |
| 9     | MediaLocating           | Windows Media Player 正在尋找媒體專案。 檔案可以是本機或遠端。                                                                      |
| 10    | MediaConnecting         | 連接到保存媒體專案的伺服器。                                                                                                    |
| 11    | MediaLoading            | 媒體專案已存在，現在正在進行取出。                                                                                                |
| 12    | MediaOpening            | 媒體專案已被取出，現在正在開啟。                                                                                                 |
| 13    | MediaOpen               | 媒體專案現在已開啟。                                                                                                                                |
| 14    | BeginCodecAcquisition   | 正在開始取得編解碼器。                                                                                                                            |
| 15    | EndCodecAcquisition     | 編解碼器取得已完成。                                                                                                                         |
| 16    | BeginLicenseAcquisition | 取得用來播放受 DRM 保護內容的授權。                                                                                                     |
| 17    | EndLicenseAcquisition   | 已取得播放受 DRM 保護內容的授權。                                                                                               |
| 18    | BeginIndividualization  | 開始 DRM 的個人化。                                                                                                                           |
| 19    | EndIndividualization    | 已完成 DRM 的個人化。                                                                                                              |
| 20    | MediaWaiting            | 正在等候媒體專案。                                                                                                                                |
| 21    | OpeningUnknownURL       | 開啟具有未知類型的 URL。                                                                                                                    |



 

## <a name="remarks"></a>備註

Windows Media Player 狀態不保證會以任何特定順序發生。 此外，並非每個狀態都一定會在一連串的事件期間發生。 您不應該撰寫依賴狀態順序的程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**OpenStateChange 事件**](player-player-openstatechange.md)
</dt> </dl>

 

 





