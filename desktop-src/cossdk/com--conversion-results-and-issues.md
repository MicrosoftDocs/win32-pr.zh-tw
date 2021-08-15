---
description: 無論您選擇手動將 MTS 套件轉換為 com + 應用程式，或讓 Microsoft Windows 安裝程式自動為您進行，您應該留意轉換的結果以及問題。
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: COM + 轉換結果和問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a347df5f0ad0b16aee509c9c1b2c2c848372d0df2ccbc376814b0d14eb61d138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129210"
---
# <a name="com-conversion-results-and-issues"></a>COM + 轉換結果和問題

無論您選擇手動將 MTS 套件轉換為 com + 應用程式，或讓 Microsoft Windows 安裝程式自動為您進行，您應該留意轉換的結果以及問題。

## <a name="what-is-converted"></a>轉換的內容

在轉換期間，MTSTOCOM 公用程式會轉換角色、角色指派、介面、方法、使用者、電腦清單，以及大部分的電腦設定。 MTSTOCOM 公用程式也會轉換 MTS 套件的身分識別和密碼。

在 MTS 中無法使用的新 COM + 屬性會自動設定為所有已轉換之 MTS 元件的下列預設值。 您可以使用 [元件服務] 系統管理工具或 COM + 系統管理介面變更這些預設值。

-   啟用 JIT 啟用。
-   物件共用已停用。
-   與交易設定相同的同步處理。

## <a name="conversion-issues"></a>轉換問題

當您安裝 Windows 時，系統會自動安裝 COM +。 不可能卸載 COM +。 與現有 MTS 和 COM + 安裝的升級相關的問題包括下列各項：

-   如果您目前使用的是 MTS 1.0，則會自動將 MTS 升級至 COM +。 不過，使用者定義的封裝將會遺失，因此您必須重新建立它們。
-   如果您目前使用的是 MTS 2.0，則會自動將 MTS 升級至 COM +。 所有使用者定義的封裝將會升級至 COM + 應用程式。 所有元件的運作方式應該與在 MTS 2.0 下的元件相同。
-   如果您使用的是 MTS 1.0 和 MTS 2.0 並已安裝 SDK 選項，將會移除 SDK 檔案。 您可以透過 Microsoft Windows SDK 安裝最新的 com + SDK。
-   您無法從 COM + 電腦管理遠端 MTS 電腦。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從 MTS 自動轉換](automatic-conversion-from-mts.md)
</dt> <dt>

[從 MTS 手動轉換](manual-conversion-from-mts.md)
</dt> <dt>

[MTS 管理程式庫](mts-administration-library.md)
</dt> </dl>

 

 



