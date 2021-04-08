---
title: 技術概觀
description: Microsoft Active Accessibility 改善協助工具輔助的方式 (特殊程式，協助殘障人士更有效地使用電腦) 使用在 Microsoft Windows 上執行的應用程式。
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674831"
---
# <a name="technical-overview"></a>技術概觀

Microsoft Active Accessibility 改善協助工具輔助的方式 (特殊程式，協助殘障人士更有效地使用電腦) 使用在 Microsoft Windows 上執行的應用程式。

Microsoft Active Accessibility 是以元件物件模型為基礎， (COM) （由 Microsoft 開發），它是一種業界標準，可定義應用程式和作業系統進行通訊的常見方式。 Microsoft Active Accessibility 是由下列元件所組成：

-   COM 介面 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，它會公開 UI 元素的相關資訊。 **IAccessible** 也有屬性和方法，可取得和操作該 UI 元素的相關資訊。
-   WinEvents，可讓伺服器在可存取的物件變更時通知用戶端的事件系統。
-   Oleacc.dll，支援或執行時間 DLL。

Oleacc.dll Microsoft Active Accessibility DLL 包含下列元件：

-   允許用戶端要求 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標的函式 (例如 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)) 。
-   允許伺服器將 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標傳回給用戶端的函式 (例如 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)) 。
-   用來取得角色和狀態碼之當地語系化文字的函式 (例如 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 和 [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)) 。
-   某些 helper 函數 ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)) 。
-   為標準使用者和 COMCTL 控制項提供 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 預設執行的程式碼。 因為這些會代表系統控制項來執行 **IAccessible** ，*所以稱為 proxy。*

## <a name="in-this-section"></a>本節內容

-   [Active Accessibility 的運作方式](how-active-accessibility-works.md)
-   [Active Accessibility 基本概念](active-accessibility-basics.md)
-   [伺服器指導方針](server-guidelines.md)
-   [用戶端指導方針](client-guidelines.md)
-   [COM 和 Unicode 指導方針](com-and-unicode-guidelines.md)

 

 




