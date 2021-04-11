---
description: 應用程式必須呼叫幾個函數才能要求功能。
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: 要求功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026984"
---
# <a name="requesting-a-feature"></a>要求功能

應用程式必須呼叫幾個函數才能要求功能。 在要求功能之前，應用程式必須確定已安裝此功能。 如果應用程式在應用程式存取功能之前呼叫 [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) ，應用程式可以使用傳回的資訊來維持使用計量。

**要求功能**

1.  如果您想要判斷功能的可用性，而不遞增使用量計數，請呼叫 [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) 或 [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) 函數。
2.  藉由呼叫 [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) 函式，指出應用程式要使用功能的意圖。
3.  藉由呼叫 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 函數來判斷檔案位置。
4.  藉由呼叫 [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) 函數來設定此功能。
5.  藉由呼叫 [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) 函數來取得應用程式可使用的使用計量。

下圖說明功能要求模型。

![功能要求模型。 ](images/over2.png)

 

 



