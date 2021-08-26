---
description: 基於安全性考慮，有時需要安全的轉換。
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: 安全的轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07c36b70827c301117bff7d98b30aae2990efb80f892bda24b0be35cbba5316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040838"
---
# <a name="secured-transforms"></a>安全的轉換

基於安全性考慮，有時需要安全的轉換。 安全的轉換會儲存在使用者電腦本機的位置，在安全的檔案系統上，使用者沒有寫入權限。 在安裝或公告封裝期間，此位置會快取這類轉換。 只有系統管理員和本機系統具有這個位置的寫入權限。 非管理使用者無法修改轉換檔案。 在後續 [安裝隨選安裝](installation-on-demand.md) 或封裝的 [維護安裝](maintenance-installation.md) 期間，安裝程式會使用快取的轉換。

若要指定安全的轉換儲存區，請設定 [TransformsSecure 原則](transformssecure-policy.md)、設定 [**TransformsSecure**](transformssecure.md) 屬性，或 \| 在轉換清單中傳遞 @ 或符號。 請注意，您不能在相同的轉換清單中包含安全且不安全的轉換。 請參閱套用 [轉換](applying-transforms.md)。

任何使用者移除產品時，都會從使用者的電腦移除該產品的所有安全轉換。

如果安裝程式發現安全的轉換無法在本機使用，則會嘗試從來源還原轉換快取。 安全轉換可以是安全的來源或安全的-完整路徑：

-   本機轉換快取中遺失的[安全來源轉換](secure-at-source-transforms.md)會從 .msi 檔來源的根目錄還原。
-   本機轉換快取中遺失的[安全-完整路徑轉換](secure-full-path-transforms.md)會從轉換清單所指定的原始完整路徑還原。

 

 



