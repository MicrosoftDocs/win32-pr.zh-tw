---
title: 無法 Windows Store 應用程式使用 MSAA
description: 無法 Windows Store 應用程式使用 MSAA
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabfd0f855cc4d3940a68fd18e69c4ca2a93774ccdbd0fb1868d2f8f489abea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935078"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>無法 Windows Store 應用程式使用 MSAA

## <a name="platform"></a>平台

**用戶端**– Windows 8 


## <a name="description"></a>描述

Windows 8 不支援從 Windows Store 應用程式讀取或自動化可存取資料的 MSAA (Microsoft Active Accessibility) 。 您應改為使用消費者介面自動化 (UIA) API （自 Windows 7 起提供）。 因為沒有任何現有的 Windows 存放區應用程式功能，所以沒有受此變更影響的現有實施。 這只會影響針對 Windows 8 所撰寫的新應用程式和功能。 開發人員仍然可以使用 MSAA 來公開其協助工具資料。 如果 MSAA 資料是由 Windows Store 應用程式提供者所提供，UIA 用戶端仍然可以讀取資料並將其自動化。

為了簡化 Windows 8Windows Store 應用程式的 API，我們決定只支援消費者介面自動化作為這些應用程式的用戶端。 UIA 用戶端可以原生方式讀取 UIA 提供者，而不會轉譯。 UIA 用戶端可以讀取 MSAA 提供者，以透過 UIA 對 MSAA Proxy 轉譯。 這可降低 Windows Store 應用程式開發人員的測試負擔。

消除 MSAA 提供者的支援可進一步減少測試矩陣，但是有主要的應用程式仍然是 MSAA 型，我們不想要將它們轉譯為無法存取。

## <a name="manifestation"></a>表現

WindowsStore 應用程式開發人員將無法在應用程式模型記憶體取 MSAA 的詳細資料。

## <a name="solution"></a>解決方案

對於 Windows Store 應用程式的功能，不應在 MSAA 中撰寫新的自動化案例。

如果有任何現有的現成可用工具需要與 Windows Store 應用程式互動，請將其切換為 UIA。 WindowsStore 應用程式開發人員應該使用消費者介面自動化 API。

## <a name="resources"></a>資源

-   [UI 自動化基礎](../winauto/entry-uiauto-win32.md)

 

 