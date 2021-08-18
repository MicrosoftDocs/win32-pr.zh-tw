---
description: 有幾個功能會變更產品元件和功能的安裝。 以下說明如何變更功能和元件。
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: 使用功能和元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b77fd93a9f2ee8181020f6c436d7e61e09a0f6d7858f0159fb70a7c7d8eeef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145171"
---
# <a name="working-with-features-and-components"></a>使用功能和元件

有幾個功能會變更產品 [元件和功能](components-and-features.md)的安裝。 以下說明如何變更功能和元件。

**變更功能和元件的安裝**

1.  藉由呼叫 [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) 函數來設定元件或功能的安裝層級。

    封裝中的每項功能都會被指派 [功能資料表](feature-table.md)中的安裝層級。 如果功能的安裝層級低於 [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)所設定的層級，則會選取此功能進行安裝。 呼叫 **MsiSetInstallLevel** 之後，您可以明確變更是否已安裝功能。

2.  藉由呼叫 [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) 函式來判斷指定功能可使用的狀態。
3.  藉由呼叫 [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) 函式，取得指定功能及其子功能的磁碟空間需求。
4.  藉由呼叫 [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) 函式或 [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) 函數來取得功能或元件的目前狀態。
5.  使用 [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) 函數或 [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) 函數來變更功能或元件的狀態。

 

 



