---
title: 標記
description: 標記
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK，標記
- Advanced Systems Format (ASF) ，標記
- ASF (Advanced Systems Format) ，標記
- 標記，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840776"
---
# <a name="markers"></a>標記

標記是在 ASF 檔案的時間軸上命名的位置。 每個標記都有您指派的名稱和呈現時間。 您可以指定檔案所需數量的標記。

標記適用于將大型 ASF 檔案分割為邏輯片段。 使用 reader 物件播放 ASF 檔案的應用程式，可以讓使用者選擇從標記跳至標記，以簡化數位媒體的導覽。 例如，如果您要將 ASF 檔案從簡報中移出，您可以在時間軸中，為每個討論的主要主題放入標記。 在播放時，使用者可以直接從清單中挑選主題，並直接移至檔案的相關部分，而不是取得一長時間的時間軸，而且必須在要搜尋的位置上猜測。

標記是由中繼資料編輯器物件操作。 寫入檔案之後，您隨時都可以新增、移除和查看檔案中的標記。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**搜尋標記**](to-seek-to-markers.md)
</dt> <dt>

[**使用標記**](using-markers.md)
</dt> </dl>

 

 




