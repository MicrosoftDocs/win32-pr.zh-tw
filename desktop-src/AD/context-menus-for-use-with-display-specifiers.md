---
title: 用於顯示規範的內容功能表
description: Active Directory 系統管理 MMC 嵌入式管理單元和 Windows 2000 shell 會提供一種機制，將專案新增至 Active Directory Domain Services 中物件所顯示的內容功能表。
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- 顯示規範廣告，內容功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b55b530797f1ac43456606d0fecf30e7641bf10399fb3c074135a3e0c49fd0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021705"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>用於顯示規範的內容功能表

Active Directory 系統管理 MMC 嵌入式管理單元和 Windows 2000 shell 會提供一種機制，將專案新增至 Active Directory Domain Services 中物件所顯示的內容功能表。 您可以藉由實作為 *內容功能表延伸* 的 COM 內部進程伺服器來加入內容功能表項目。 您也可以新增操作功能表項目，以叫用任何以 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API 啟動的檔案，例如應用程式或網頁 URL。 這就是所謂的 *靜態內容功能表項目*。

## <a name="developer-audience"></a>開發人員讀者

本檔假設讀者已熟悉使用 c + + 的 COM 作業和元件開發。 目前無法使用 Microsoft Visual Basic 來建立 Active Directory Domain Services 內容功能表延伸模組。

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>使用內容功能表延伸模組擴充內容功能表

內容功能表延伸模組是一種 COM 內伺服器，會執行特定的介面並向 Active Directory Domain Services 註冊。

**建立和安裝內容功能表延伸模組**

1.  建立內容功能表延伸模組 DLL。 內容功能表延伸是 COM 的內部伺服器伺服器，至少會執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面。 如需詳細資訊，請參閱 [執行內容功能表 COM 物件](implementing-the-context-menu-com-object.md)。
2.  在使用內容功能表延伸的電腦上安裝內容功能表表擴充功能。 您可以建立內容功能表延伸模組 DLL 的 Microsoft Windows Installer 套件，並使用群組原則適當地部署封裝，以達成此目的。 如需詳細資訊，請參閱散發 [消費者介面元件](distributing-user-interface-components.md)。
3.  在 Windows 登錄和 Active Directory Domain Services 中註冊內容功能表延伸模組。 如需詳細資訊，請參閱 [在顯示規範中註冊內容功能表 COM 物件](registering-the-context-menu-com-object-in-a-display-specifier.md)。

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>使用靜態內容功能表項目擴充內容功能表

靜態內容功能表項目可用來叫用任何以 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API 啟動的檔案，例如應用程式或網頁 URL。 若要完成這項作業，必須註冊特定物件類別的靜態內容功能表項目，以便將靜態內容功能表項目加入至該類別之物件的內容功能表。 如需詳細資訊，請參閱 [註冊靜態內容功能表項目](registering-a-static-context-menu-item.md)。

 

 