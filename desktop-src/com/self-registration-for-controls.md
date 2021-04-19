---
title: 控制項的自我註冊
description: 控制項的自我註冊
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965256"
---
# <a name="self-registration-for-controls"></a>控制項的自我註冊

ActiveX 控制項必須藉由執行 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 函式，支援自我註冊。 ActiveX 控制項必須註冊可内嵌物件和 automation 伺服器的所有標準登錄專案。

ActiveX 控制項必須使用元件類別 API 將本身註冊為控制項，並註冊元件類別以要求主機支援，以及控制項所執行的任何類別，請參閱 [元件類別](component-categories.md)。

ActiveX 控制項也應登錄 [ToolBoxBitmap32](toolboxbitmap32.md) 登錄機碼，不過這不是必要的。

只有當控制項適合用來做為複合檔案物件時，才應該註冊可插入的元件類別目錄。 請務必注意，複合檔案物件必須支援 ActiveX 控制項所需的最小 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 以外的特定介面。 雖然 ActiveX 控制項可能會限定為複合檔案物件，但控制項的檔應該清楚陳述在這些情況下所預期的行為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項](controls.md)
</dt> </dl>

 

 