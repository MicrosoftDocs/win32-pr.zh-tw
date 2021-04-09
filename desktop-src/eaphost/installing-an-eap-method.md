---
title: 安裝 EAP 方法
description: 請遵循下列指示，在執行 EAPHost 的用戶端電腦上安裝使用者所執行的 EAP 方法。
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682104"
---
# <a name="installing-an-eap-method"></a><span data-ttu-id="2f613-103">安裝 EAP 方法</span><span class="sxs-lookup"><span data-stu-id="2f613-103">Installing an EAP Method</span></span>

<span data-ttu-id="2f613-104">請遵循下列指示，在執行 EAPHost 的用戶端電腦上安裝使用者所執行的 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="2f613-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="2f613-105">為您的 EAP 方法 DLL 執行 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 。</span><span class="sxs-lookup"><span data-stu-id="2f613-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="2f613-106">這些函式會在安裝期間為您的 EAP 方法新增和移除適當的登錄機碼，並 (卸載) 進程。</span><span class="sxs-lookup"><span data-stu-id="2f613-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="2f613-107">如需與 EAP 方法安裝相關聯之特定登錄機碼的詳細資訊，請參閱 [Eap 方法](registry-keys-for-eap-methods.md) 的登錄設定主題。</span><span class="sxs-lookup"><span data-stu-id="2f613-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="2f613-108">使用下列主控台命令安裝含有 EAP 方法的 DLL。</span><span class="sxs-lookup"><span data-stu-id="2f613-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="2f613-109">**regsvr32.exe** *&lt; DLL 名稱 &gt;*</span><span class="sxs-lookup"><span data-stu-id="2f613-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="2f613-110">若要卸載 DLL，請使用下列主控台命令：</span><span class="sxs-lookup"><span data-stu-id="2f613-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="2f613-111">**regsvr32.exe** **/u** *&lt; DLL 名稱 &gt;*</span><span class="sxs-lookup"><span data-stu-id="2f613-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="2f613-112">重新開機 EAPHost 服務。</span><span class="sxs-lookup"><span data-stu-id="2f613-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f613-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f613-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f613-114">使用 EAPHost</span><span class="sxs-lookup"><span data-stu-id="2f613-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 