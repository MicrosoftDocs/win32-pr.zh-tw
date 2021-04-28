---
description: 一般規則是桌面應用程式可以呼叫 Windows 執行階段 (WinRT) API。 不過，某些 Api （包括 XAML UI Api）要求呼叫應用程式必須有套件身分識別。
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: 從桌面應用程式呼叫的 WinRT Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172480"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>從桌面應用程式呼叫的 WinRT Api

Desktop ( .NET 和原生 c + +) 應用程式都可以使用大部分的 [Windows 執行階段 (WinRT) api](/uwp/api/) 。 不過，某些 WinRT 類別是針對所設計，且僅支援在 UWP 應用程式中使用。 這包括 [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher)、 [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow)、 [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)和一些相關類別。 其他 WinRT 類別可在桌面應用程式中運作，但特定成員除外。

如需詳細資訊，請參閱 [Windows 執行階段桌面應用程式中不支援的 api](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api)。 如有提供，本文建議替代 Api，以達成與不支援的 Api 相同的功能。
