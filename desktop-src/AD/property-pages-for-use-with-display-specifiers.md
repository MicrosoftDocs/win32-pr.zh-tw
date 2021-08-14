---
title: 搭配顯示規範使用的屬性頁
description: Active Directory Domain Services 提供一種機制，讓您可以從 Active Directory 系統管理嵌入式管理單元或 Windows shell，將頁面新增至顯示的屬性工作表。
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- 顯示指定名稱 AD、屬性頁以用於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f813223aa88dce3b8bba867139bab476416cba1932c583e2e9be591de03fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185182"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>搭配顯示規範使用的屬性頁

Active Directory Domain Services 提供一種機制，讓您可以從 Active Directory 系統管理嵌入式管理單元或 Windows shell，將頁面新增至顯示的屬性工作表。 若要將頁面加入至屬性工作表，請執行屬性工作表延伸。

## <a name="developer-audience"></a>開發人員讀者

本檔假設讀者已熟悉使用 c + + 的 COM 作業和元件開發。 目前無法使用 Visual Basic 建立 Active Directory 的屬性工作表延伸模組。

## <a name="creating-an-active-directory-property-sheet-extension"></a>建立 Active Directory 屬性工作表延伸模組

*屬性工作表延伸* 模組是內部進程伺服器，會執行特定的介面並向 Active Directory Domain Services 註冊。 若要建立屬性工作表延伸模組，請執行下列步驟。

**若要建立 Active Directory 屬性工作表延伸模組**

1.  建立屬性工作表延伸模組 DLL。 屬性工作表延伸是 COM 的內部伺服器伺服器，至少會執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面。 如需詳細資訊，請參閱 [執行屬性頁面 COM 物件](implementing-the-property-page-com-object.md)。
2.  在要使用屬性工作表擴充功能的電腦上安裝屬性工作表延伸模組。 若要這樣做，請為屬性工作表延伸 DLL 建立 Microsoft Windows Installer 套件，並使用群組原則適當地部署套件。 如需詳細資訊，請參閱散發 [消費者介面元件](distributing-user-interface-components.md)。
3.  在 Windows 登錄和 Active Directory Domain Services 中註冊屬性工作表延伸模組。 如需詳細資訊，請參閱 [在顯示規範中註冊屬性頁 COM 物件](registering-the-property-page-com-object-in-a-display-specifier.md)。

 

 