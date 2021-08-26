---
description: 作者應該先針對每個新的或新修改的合併模組執行驗證，再嘗試將模組第一次合併到安裝資料庫中。
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: 驗證合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5a226f72e35ce4ee76599444e86ef80bd71a8866ca80eef2a5da04a87fb79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995797"
---
# <a name="validating-merge-modules"></a>驗證合併模組

作者應該先針對每個新的或新修改的合併模組執行驗證，再嘗試將模組第一次合併到安裝資料庫中。 合併模組驗證的運作方式與 [封裝驗證](package-validation.md) 相同，但會使用不同的 [內部一致性評估](internal-consistency-evaluators-ices.md) 工具集， (適用于合併模組的特定) 。 如需有關這些 merge module 的詳細資訊，請參閱 [合併模組 ICE 參考](merge-module-ice-reference.md)。

Merge module 會儲存在 merge module 的 .cub 檔中，Mergemod。 安裝 Orca 工具或 msival2 時，也會提供標誌 .cub、Darice 和 Mergemod。

如需詳細資訊，請參閱 [合併模組 ICE 參考](merge-module-ice-reference.md)。

 

 



