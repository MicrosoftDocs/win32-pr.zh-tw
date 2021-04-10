---
title: " (已淘汰) 建立 Windows Media 下載套件"
description: " (已淘汰) 建立 Windows Media 下載套件"
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- Windows Media 下載套件，建立
- 建立 Windows Media 下載套件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021654"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a> (已淘汰) 建立 Windows Media 下載套件

本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。

請遵循下列步驟來建立 Windows Media 下載套件。

1.  **建立框線。** 使用您用來建立 Windows Media Player 面板的相同技術。 設計框線，以便調整大小 Windows Media Player 不會損毀框線元素的組合。 例如，使用純色或視覺效果做為背景，因為在調整大小 Windows Media Player 時，將會相應縮小。
2.  **壓縮框線內容。** 建立副檔名為 .zip 的壓縮資料夾 () 包含 border 檔案：影像、JScript 檔案，以及具有 wms 副檔名的外觀定義檔。 重新命名壓縮檔案，使其副檔名為 wmz。
3.  **撰寫 Windows Media 中繼檔。** 除非您建立的 Windows Media 中繼檔的副檔名為 **.asx，否則** Windows Media Player 不會載入框線。 中繼檔也可以用來建立播放清單，以描述套件中所含的內容。
4.  **組合您的內容。** 將您想要使用的所有檔案放在資料夾中。 這包括音訊檔案、影片檔案、中繼檔和框線定義檔。
5.  **建立套件。** 建立副檔名為 .zip 的壓縮資料夾 () ，其中包含 border 檔案、內容檔案和中繼檔。 將這個 .zip 檔案的副檔名變更為 wmd 副檔名。
6.  **將套件張貼至網站。** 完成的封裝已準備好發佈至網站，並由使用者下載。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**(淘汰的 Windows Media 下載套件)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




