---
description: 若要將專案新增至 [程式] 子功能表，請遵循下列步驟。
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: 如何在 [開始] 功能表中新增快捷方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115513"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>如何在 [開始] 功能表中新增快捷方式

若要將專案新增至 [ **程式** ] 子功能表，請遵循下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)介面建立 [shell 連結](./links.md)。

### <a name="step-2"></a>步驟 2:

使用 [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 函式，傳遞 [**FOLDERID \_ 程式**](knownfolderid.md)來取得程式資料夾的位置。

### <a name="step-3"></a>步驟 3：

將 Shell 連結新增至 [程式] 資料夾。 您也可以在 [程式] 資料夾中建立資料夾，並將連結新增至該資料夾。

 

 
