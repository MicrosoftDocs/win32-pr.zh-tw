---
title: 註冊元件
description: 註冊元件
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024133"
---
# <a name="registering-components"></a><span data-ttu-id="22ea6-103">註冊元件</span><span class="sxs-lookup"><span data-stu-id="22ea6-103">Registering Components</span></span>

<span data-ttu-id="22ea6-104">安裝下列類型的應用程式時，必須將安裝資訊新增至登錄，通常是透過安裝程式：</span><span class="sxs-lookup"><span data-stu-id="22ea6-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="22ea6-105">伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="22ea6-105">Server applications</span></span>
-   <span data-ttu-id="22ea6-106">容器/伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="22ea6-106">Container/server applications</span></span>
-   <span data-ttu-id="22ea6-107">允許連結至内嵌物件的容器應用程式</span><span class="sxs-lookup"><span data-stu-id="22ea6-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="22ea6-108">對於這三個實例，請註冊 COM 程式庫 (DLL) 資訊和應用程式特定資訊。</span><span class="sxs-lookup"><span data-stu-id="22ea6-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="22ea6-109">DLL 會匯出 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)，以註冊其所有元件的資訊。</span><span class="sxs-lookup"><span data-stu-id="22ea6-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="22ea6-110">使用下列函式來註冊和取消註冊元件：</span><span class="sxs-lookup"><span data-stu-id="22ea6-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="22ea6-111">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="22ea6-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="22ea6-112">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="22ea6-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="22ea6-113">**RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="22ea6-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="22ea6-114">**RegEnumKeyEx**</span><span class="sxs-lookup"><span data-stu-id="22ea6-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="22ea6-115">**RegDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="22ea6-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="22ea6-116">**RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="22ea6-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="22ea6-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="22ea6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22ea6-118">註冊 COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="22ea6-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 