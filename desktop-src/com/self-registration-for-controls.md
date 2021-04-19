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
# <a name="self-registration-for-controls"></a><span data-ttu-id="5c5b7-103">控制項的自我註冊</span><span class="sxs-lookup"><span data-stu-id="5c5b7-103">Self Registration for Controls</span></span>

<span data-ttu-id="5c5b7-104">ActiveX 控制項必須藉由執行 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 函式，支援自我註冊。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="5c5b7-105">ActiveX 控制項必須註冊可内嵌物件和 automation 伺服器的所有標準登錄專案。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="5c5b7-106">ActiveX 控制項必須使用元件類別 API 將本身註冊為控制項，並註冊元件類別以要求主機支援，以及控制項所執行的任何類別，請參閱 [元件類別](component-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="5c5b7-107">ActiveX 控制項也應登錄 [ToolBoxBitmap32](toolboxbitmap32.md) 登錄機碼，不過這不是必要的。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="5c5b7-108">只有當控制項適合用來做為複合檔案物件時，才應該註冊可插入的元件類別目錄。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="5c5b7-109">請務必注意，複合檔案物件必須支援 ActiveX 控制項所需的最小 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 以外的特定介面。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="5c5b7-110">雖然 ActiveX 控制項可能會限定為複合檔案物件，但控制項的檔應該清楚陳述在這些情況下所預期的行為。</span><span class="sxs-lookup"><span data-stu-id="5c5b7-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c5b7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c5b7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c5b7-112">控制項</span><span class="sxs-lookup"><span data-stu-id="5c5b7-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 