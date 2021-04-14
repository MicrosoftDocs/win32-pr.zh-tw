---
title: 管理記憶體配置
description: 管理記憶體配置
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383010"
---
# <a name="managing-memory-allocation"></a>管理記憶體配置

在 COM 中，許多（如果不是大多數）介面方法是由一個程式設計組織所撰寫，並由另一個程式碼所撰寫的程式碼所呼叫。 這些函式的許多參數和傳回值都是可透過傳值方式傳遞的類型。 不過，有時候必須傳遞資料結構，而不是這種情況，因此呼叫端和呼叫都必須有相容的配置和取消配置原則。 COM 會定義記憶體配置的通用慣例，因為它比定義個案規則更合理，因此 COM 遠端程序呼叫的執行可以正確地管理記憶體。

COM 介面的方法一律會藉由呼叫 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面中找到的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)函式，來提供介面指標的記憶體管理，而所有其他 COM 介面都會從該介面衍生。  (參閱 [管理參考計數的規則](rules-for-managing-reference-counts.md) ，以取得詳細資訊。 ) 

本節只會說明如何針對未以傳值方式傳遞的參數配置記憶體（不是介面指標），還會描述更常見的專案，例如字串、結構指標等等。

如需詳細資訊，請參閱下列主題：

-   [OLE 記憶體配置器](the-ole-memory-allocator.md)
-   [記憶體管理規則](memory-management-rules.md)
-   [調試記憶體配置](debugging-memory-allocations.md)

 

 