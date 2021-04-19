---
title: DownloadCollection. startDownload 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 StartDownload 方法會將下載排在佇列中。
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- startDownload 方法 Windows Media Player
- startDownload 方法 Windows Media Player，DownloadCollection 類別
- DownloadCollection 類別 Windows Media Player，startDownload 方法
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990958"
---
# <a name="downloadcollectionstartdownload-method"></a>DownloadCollection. startDownload 方法

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**StartDownload** 方法會將下載排在佇列中。

## <a name="syntax"></a>語法


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sourceURL* \[在\]
</dt> <dd>

**字串** ，指定下載的 URL。

</dd> <dt>

*類型* \[在\]
</dt> <dd>

指定下載類型的 **字串**。 包含下列其中一個值。



| 值      | 描述                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 背景資訊 |  (Windows XP 及更新版本。 ) 下載會在處理器時間變成可用時，做為背景進程。 即使在 Windows Media Player 或 Windows XP 關閉時，下載狀態仍會保存。 |
| 即時  |  (所有支援的作業系統。 ) 下載會一次完成。 會話之間不會保存任何下載狀態。                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **DownloadItem** 物件。

## <a name="remarks"></a>備註

當新的下載開始時，下載管理員會將它以專案的形式新增至起始下載的下載集合。

只有下列數位媒體格式可供下載：

-   進階系統格式 (ASF)
-   MP3
-   Windows Media 音訊 (WMA)
-   Windows Media 視訊 (WMV)

*SourceURL* 參數不支援 Unicode 編碼字串。 它必須指向有效的內容。 不支援重新導向。

使用 Windows XP 時，會根據檔案層級的中繼資料值，將音訊檔案自動放入適當的「 **我的音樂** 」子資料夾。 影片檔案會放入 \\ 我的音樂 \\ 下載 \\ *亂數* \\ *型* 別，其中 *亂數字* 是每個使用者 Windows Media Player 所產生的隨機值，而 *類型* 則為 "real time" 或 "background" （視下載類型而定）。

在 windows 98 和 windows Millennium Edition (ME) 中使用 Windows Media Player 9 系列時，會將音訊和影片檔案放入 \\ 我的音樂 \\ 下載的 \\ *亂數字* \\ *類型*，其中 *亂數字* 是播放程式為每位使用者產生的隨機值，而 *類型* 則為 "real time" 或 "background" （視下載類型而定）。

請注意，檔案可能會根據檔案中包含的中繼資料屬性，以及使用者在 [ **選項** ] 對話方塊中指定的規則來重新命名。 未包含中繼資料的檔案（如 **專輯** 或 **演出者**）可能會移至標示為「未知演出者」或「未知專輯」的資料夾。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadCollection 物件**](downloadcollection-object.md)
</dt> <dt>

[**DownloadItem 物件**](downloaditem-object.md)
</dt> </dl>

 

 





