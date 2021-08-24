---
description: 在升級期間，以及透過相關應用程式安裝新的應用程式時，會使用 MigrateFeatureStates 動作。
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: MigrateFeatureStates 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac96a3b2babf5f92ae8078ecc703875c09a0e2f61155fd565985919b5a6393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745168"
---
# <a name="migratefeaturestates-action"></a>MigrateFeatureStates 動作

在升級期間，以及透過相關應用程式安裝新的應用程式時，會使用 MigrateFeatureStates 動作。 MigrateFeatureStates 會讀取現有應用程式中的功能狀態，然後在擱置安裝中設定這些功能狀態。 只有當新的功能樹狀結構並未大幅地從原始的變更時，此方法才有用。

只有在第一次安裝產品時，才會執行 MigrateFeatureStates 動作。 MigrateFeatureStates 動作不會在維護模式或卸載期間執行。

MigrateFeatureStates 動作會依序執行每個 [升級資料表](upgrade-table.md) 的記錄，並將每個資料列中的升級程式碼、產品版本和語言，與系統上安裝的所有產品進行比較。 如果 MigrateFeatureStates 動作偵測到通訊，而且在升級資料表的 [屬性] 資料行中設定 msidbUpgradeAttributesMigrateFeatures 位旗標，則安裝程式會查詢產品的現有功能狀態，並針對新應用程式中的相同功能設定這些狀態。 只有未設定 [**預先**](preselected.md) 選取的屬性時，動作才會遷移功能狀態。

## <a name="sequence-restrictions"></a>順序限制

MigrateFeatureStates 動作應該緊接在 [CostFinalize 動作](costfinalize-action.md)之後。 MigrateFeatureStates 必須在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中排序。 如果動作已在 InstallUISequence 中執行，則安裝程式會防止 MigrateFeatureStates 在 InstallExecuteSequence 中執行。

## <a name="actiondata-messages"></a>ActionData 訊息

MigrateFeatureSettings 會傳送每項產品的動作資料訊息。

## <a name="remarks"></a>備註

如果有多個已安裝的產品共用功能，則該功能的安裝狀態可能會在產品之間不同。 MigrateFeatureState 動作在遷移功能安裝狀態時，會使用下列優先順序：執行本機、從來源執行、公告和卸載。 例如，已安裝的產品 A 可能具有 INSTALLSTATE 本機的功能 Y \_ ，且安裝的產品 B 可能會有功能 y，因為 INSTALLSTATE 不 \_ 存在。 如果升級會安裝產品 C 並遷移功能 Y 的安裝狀態，MigrateFeatureState 會將 product C 中的功能 Y 安裝狀態設定為 INSTALLSTATE \_ LOCAL。

如需有關如何使用 MigrateFeatureStates 動作進行產品升級的詳細資訊，請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。

 

 



