---
title: 原生 IAccessible 支援
description: Oleacc.dll 代表 OBJID \_ CLIENT \ 160 執行 IAccIdentity，IAccessible 介面指標和其直屬簡單元素子系。
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad499b96c668349cc481efd388a780ba094eff2ef6eb4ae52ab041aabea70fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565046"
---
# <a name="native-iaccessible-support"></a>原生 IAccessible 支援

Oleacc.dll 代表 [**OBJID \_ 用戶端**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標及其立即的簡單元素子系來執行 [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) 。 當包含 *lParam*  OBJID 用戶端的 [**WM \_ GETOBJECT**](wm-getobject.md)傳送至 HWND （代表視窗的工作區或整個控制項）時，就會傳回 **OBJID \_ 用戶端** IAccessible 介面指標  =  **\_** 。  這類 **IAccessible** 介面指標的父系通常會有 [**角色 \_ 系統 \_ 視窗**](object-roles.md)的角色，而且是將包含 *lParam* OBJID 視窗的 **WM \_ GETOBJECT**  =  [**\_**](object-identifiers.md)傳送至 hwnd 時所傳回的 IAccessible 物件。

這些 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標通常會發生在 Oleacc.dll proxy 子類別化，或簡單自訂控制項 (例如容器 **IAccessible** 加上一層簡單元素子系) 提供原生 IAccessible 實作為原生 。

更複雜的原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行，例如 **IAccessible** 的階層存在或使用自訂物件識別碼時，必須自行執行 [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) 。

 

 




