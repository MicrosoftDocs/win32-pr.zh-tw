---
description: 產生新的修補程式可能需要很長的時間。
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: '修補資訊快取 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71513ea1a9418506bbf9025f66a1689c12e9a53f8e6f2e713ddeb3b3d55de580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942619"
---
# <a name="patch-information-caching-patchwizdll"></a>修補資訊快取 (Patchwiz.dll) 

產生新的修補程式可能需要很長的時間。 使用 [Patchwiz.dll](patchwiz-dll.md)產生修補程式之後，您可能需要再次變更更新映射，並產生另一個修補程式。 修補資訊快取可以藉由重複使用現有的修補程式，來減少產生後續修補程式所需的時間。 例如，您可以使用先前修補程式所產生的二進位修補程式，來減少建立 service pack 所需的時間。 Patchwiz.dll 可以使用 PATCH \_ CACHE \_ DIR 找出現有的二進位修補程式，並將它新增至 service pack 的封包，而不需要重新建立二進位修補程式。

修補資訊快取需要使用 [Patchwiz.dll](patchwiz-dll.md)。 若要啟動修補程式快取， \_ 請 \_ \_ \_ 在 pcp 檔案) 的 patch 建立 ( 屬性檔 [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 中，將 [已啟用修補快取] 和 [修補快取目錄] 屬性設定為 [內容] 資料表。 Patchwiz 會將所有修補程式建立資訊儲存在 PATCH CACHE DIR 屬性所識別的資料夾中 \_ \_ ，並視需要建立此資料夾。 下次當您嘗試建立修補程式時，Patchwiz 會檢查此資料夾，以查看要比較的檔案是否符合快取中的檔案。 如果檔案相符，Patchwiz 會使用快取的資訊，而不是重新產生檔案的二進位修補程式。 如果檔案不相符，或快取中缺少資訊，Patchwiz 會產生檔案的修補程式。

若要使用修補程式資訊快取， \_ 建立 .msp 檔之後，必須保留 patch CACHE DIR 所指定的資料夾 \_ 。 如果刪除資料夾，PatchWiz 必須重新產生二進位修補程式，以取得後續的 .msp 檔案。 如需在目標檔案的選定區域中保留資訊的詳細資訊，請參閱 [修補檔案的選取區域](patching-selected-regions-of-a-file.md)。

 

 



