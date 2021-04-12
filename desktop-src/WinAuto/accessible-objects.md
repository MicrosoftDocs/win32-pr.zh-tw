---
title: 可存取的物件
description: 使用 Microsoft Active Accessibility，會將 UI 專案公開給用戶端，做為元件物件模型 (COM) 物件。
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372606"
---
# <a name="accessible-objects"></a>可存取的物件

使用 Microsoft Active Accessibility，會將 UI 專案公開給用戶端，做為元件物件模型 (COM) 物件。 這些 *可存取的物件* 會維護一些資訊，稱為「 *屬性*」（property），描述物件的名稱、畫面位置，以及協助工具輔助程式所需的其他資訊。 可存取的物件也會提供用戶端呼叫的 *方法* ，以使物件執行某些動作。 具有相關聯之簡單元素的可存取物件也稱為 *父代* 或 *容器*。

可存取的物件是使用 Microsoft Active Accessibility 的 COM 型 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面來執行。 **IAccessible** 方法和屬性可讓用戶端應用程式取得使用者所需 UI 元素的相關資訊。 例如， [**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 會將介面指標傳回給可存取物件的父系，而 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 會提供方法，讓用戶端取得容器內其他物件的相關資訊。

如需有關可存取物件和簡單元素如何相關的詳細資訊，請參閱 [簡單元素](simple-elements.md)。

 

 




