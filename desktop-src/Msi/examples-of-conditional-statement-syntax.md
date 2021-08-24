---
description: 以下提供一些常見的條件陳述式實例。 如需詳細資訊，請參閱條件陳述式語法。
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: 條件陳述式語法的範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88445e1e4b371669c43b47d1ca54e9fd677c5414985ade3908b95e00717de887
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811028"
---
# <a name="examples-of-conditional-statement-syntax"></a>條件陳述式語法的範例

以下提供一些常見的條件陳述式實例。 如需詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

## <a name="run-action-on-removal"></a>移除時執行動作。

如需詳細資訊，請參閱 [移除時要執行的調節動作](conditioning-actions-to-run-during-removal.md)。

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>只有在尚未安裝產品時，才執行動作。

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>只有在將產品安裝在本機時，才執行動作。 請勿在重新安裝時執行動作。

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

「&功能人員 = 3」一詞表示動作是在本機安裝功能。 「不 (！」一詞功能說明 = 3) 」表示功能未安裝在本機。

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>只有在即將卸載功能時，才執行動作。

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

這種情況只會檢查功能是否從本機的已安裝狀態轉換為不存在的狀態。

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>只有在元件已安裝在本機，但正在轉換為狀態時，才執行動作。

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

「？」一詞ComponetName = 3 "表示元件是安裝在本機。 「$ComponentName = 2」一詞表示元件上的動作狀態不存在。 「$ComponentName = 4」一詞表示元件上的動作狀態是從來源執行。 請注意，公告的動作狀態對元件無效。

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>只在重新安裝元件時執行動作。

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>只在套用特定修補程式時執行動作。

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

如需詳細資訊，請參閱 [ [**修補**](patch.md) ] 屬性頁上的 [備註] 區段。

 

 



