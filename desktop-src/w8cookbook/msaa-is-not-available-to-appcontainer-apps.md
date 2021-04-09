---
title: MSAA 無法供 Windows Store 應用程式使用
description: MSAA 無法供 Windows Store 應用程式使用
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024229"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA 無法供 Windows Store 應用程式使用

## <a name="platform"></a>平台

**用戶端** – Windows 8 


## <a name="description"></a>Description

Windows 8 不支援從 Windows Store 應用程式讀取或自動化可存取資料的 MSAA (Microsoft Active Accessibility) 。 消費者介面自動化 (UIA) API （自 Windows 7 起提供）應改用。 因為沒有任何現有的 Windows Store 應用程式功能，所以沒有受此變更影響的現有實施。 這只會影響針對 Windows 8 所撰寫的新應用程式和功能。 開發人員仍然可以使用 MSAA 來公開其協助工具資料。 如果 MSAA 資料是由 Windows Store 應用程式提供者所提供，UIA 用戶端仍然可以讀取資料並將其自動化。

為了簡化 Windows 8Windows Store 應用程式的 API，我們決定只支援將消費者介面自動化作為這些應用程式的用戶端。 UIA 用戶端可以原生方式讀取 UIA 提供者，而不會轉譯。 UIA 用戶端可以讀取 MSAA 提供者，以透過 UIA 對 MSAA Proxy 轉譯。 這會降低 Windows Store 應用程式開發人員的測試負擔。

消除 MSAA 提供者的支援可進一步減少測試矩陣，但是有主要的應用程式仍然是 MSAA 型，我們不想要將它們轉譯為無法存取。

## <a name="manifestation"></a>表現

Windows Store 應用程式開發人員將無法在應用程式模型記憶體取 MSAA 的詳細資料。

## <a name="solution"></a>解決方法

針對 Windows Store 應用程式的功能，不應在 MSAA 中撰寫新的自動化案例。

如果有任何現有的現成可用工具需要與 Windows Store 應用程式互動，請將其切換為 UIA。 Windows Store 應用程式開發人員應該使用消費者介面自動化 API。

## <a name="resources"></a>資源

-   [UI 自動化基礎](../winauto/entry-uiauto-win32.md)

 

 