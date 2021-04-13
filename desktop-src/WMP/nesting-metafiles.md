---
title: 嵌套中繼檔
description: 嵌套中繼檔
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Media 中繼檔，嵌套
- Windows Media 中繼檔，參考其他中繼檔
- 嵌套中繼檔
- 中繼檔，嵌套
- 中繼檔，參考其他中繼檔
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300167"
---
# <a name="nesting-metafiles"></a>嵌套中繼檔

中繼檔可以參考另一個中繼檔。 若要參考另一個中繼檔，請使用 **ENTRYREF** 元素。 主要中繼檔中的 **ENTRYREF** 元素會指向外部中繼檔。

Windows Media Player 控制項會處理參考之中繼檔的 **專案專案** ，就如同它們是包含在 **ENTRYREF** 元素位置的主要中繼檔中一樣。 但是，它會略過參考的中繼檔中，將 **SKIPIFREF** 屬性設定為 YES 的任何 **專案專案**。

Windows XP 控制項的 Windows Media Player 7.0、7.1 和 Windows Media Player 會忽略參考的中繼檔中的任何 **ENTRYREF** 元素。 因此，您只能使用這些版本來將中繼檔的深度嵌套一層。 這些版本也會忽略所參考檔案中的 **ASX** 元素及其屬性。 Windows Media Player 9 系列或更新版本支援最多5個深度的嵌套中繼檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> </dl>

 

 




