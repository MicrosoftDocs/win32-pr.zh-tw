---
title: 設定延伸模組 Dll
description: 在啟動時，NPS 會檢查登錄以取得要呼叫的協力廠商 Dll 清單。
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023795"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="c201b-103">設定延伸模組 Dll</span><span class="sxs-lookup"><span data-stu-id="c201b-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="c201b-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="c201b-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c201b-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="c201b-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c201b-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="c201b-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="c201b-107">在啟動時，NPS 會檢查登錄以取得要呼叫的協力廠商 Dll 清單。</span><span class="sxs-lookup"><span data-stu-id="c201b-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="c201b-108">若要在 NPS 伺服器上設定驗證或授權 DLL，請在下列登錄機碼底下的值列出 Dll 的路徑：</span><span class="sxs-lookup"><span data-stu-id="c201b-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="c201b-109">**HKLM \\ System \\ CurrentControlSet \\ Services \\ AuthSrv \\ 參數\\**</span><span class="sxs-lookup"><span data-stu-id="c201b-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="c201b-110">如果 **AuthSrv** 和 **Parameters** 索引鍵不存在，請加以建立。</span><span class="sxs-lookup"><span data-stu-id="c201b-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="c201b-111">要在其中列出驗證延伸模組 Dll 的值為：</span><span class="sxs-lookup"><span data-stu-id="c201b-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="c201b-112">**ExtensionDLLs**</span><span class="sxs-lookup"><span data-stu-id="c201b-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="c201b-113">要在其中列出授權延伸模組 Dll 的值為：</span><span class="sxs-lookup"><span data-stu-id="c201b-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="c201b-114">**AuthorizationDLLs**</span><span class="sxs-lookup"><span data-stu-id="c201b-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="c201b-115">**ExtensionDLLs** 和 **AuthorizationDLLs** 值都必須是 **REG \_ 多重 \_ SZ** 類型。</span><span class="sxs-lookup"><span data-stu-id="c201b-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="c201b-116">此類型可讓您列出多個 Dll。</span><span class="sxs-lookup"><span data-stu-id="c201b-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c201b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c201b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c201b-118">叫用擴充 Dll</span><span class="sxs-lookup"><span data-stu-id="c201b-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="c201b-119">使用者識別屬性</span><span class="sxs-lookup"><span data-stu-id="c201b-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 