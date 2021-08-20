---
title: 伺服器注釋
description: 本節提供使用伺服器批註的相關資訊。
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9438184cf68d4a0f819afcd7e5497e627a0982e0f9fd9784c8a3460ab5121a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052536"
---
# <a name="server-annotation"></a>伺服器注釋

本節提供使用伺服器批註的相關資訊。

## <a name="summary"></a>總結

您可以定義可執行 [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)的類別、建立其實例，以及告訴系統您希望它覆寫特定 UI 元素上的特定屬性。 當用戶端向其中一個 UI 元素要求其中一個屬性時，系統會呼叫您的物件，並提供一個值給您。 如果您的物件傳回值，則該值會傳回給用戶端。 如果您的物件不會傳回值，則會將該 UI 元素的預設值傳回給用戶端。

## <a name="when-to-use-this-technique"></a>使用這項技術的時機

當您想要覆寫物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性時，請使用這項技術。 這項技術比先前的 **IAccessible** 技巧簡單許多。 如需詳細資訊，請參閱 [動態注釋的替代方案](alternatives-to-dynamic-annotation.md)。

您無法使用伺服器注釋來改變公開的物件結構。 若要變更物件的結構，您必須執行完整的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。

如需有關伺服器批註的詳細資訊，請參閱下列主題：

-   [使用伺服器注釋](using-server-annotation.md)
-   [伺服器批註範例](server-annotation-sample.md)

 

 




