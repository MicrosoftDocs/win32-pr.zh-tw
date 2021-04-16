---
title: 類別和伺服器
description: 類別和伺服器
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382965"
---
# <a name="classes-and-servers"></a><span data-ttu-id="a34a0-103">類別和伺服器</span><span class="sxs-lookup"><span data-stu-id="a34a0-103">Classes and Servers</span></span>

<span data-ttu-id="a34a0-104">COM 使用 **HKEY \_ 類別 \_ ROOT** 進行全電腦設定，但也允許個別使用者設定 clsid，以提供更高的安全性和彈性。</span><span class="sxs-lookup"><span data-stu-id="a34a0-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="a34a0-105">COM 先諮詢 **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ 類別** ，然後才在 **HKEY \_ 類別 \_ 根目錄** 下進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="a34a0-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="a34a0-106">COM 會將電腦範圍資訊與 **HKEY \_ 類別 \_ 根目錄 \\ CLSID** 下的 clsid 保持相關，並將每個使用者的類別資訊保留在 **HKEY 的 \_ 目前 \_ 使用者 \\ 軟體 \\ 類別 \\ clsid**。</span><span class="sxs-lookup"><span data-stu-id="a34a0-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="a34a0-107">COM 伺服器支援自我註冊。</span><span class="sxs-lookup"><span data-stu-id="a34a0-107">COM servers support self-registration.</span></span> <span data-ttu-id="a34a0-108">針對同進程伺服器，這表示 DLL 必須匯出下列函數：</span><span class="sxs-lookup"><span data-stu-id="a34a0-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="a34a0-109">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="a34a0-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="a34a0-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="a34a0-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="a34a0-111">您必須使用模組定義檔、連結器參數或編譯器指示詞，明確地匯出這些函數。</span><span class="sxs-lookup"><span data-stu-id="a34a0-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="a34a0-112">類別存放區會在下載檔案至用戶端電腦之後，使用這些函數來設定本機登錄。</span><span class="sxs-lookup"><span data-stu-id="a34a0-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="a34a0-113">除了類別存放區之外，其他環境也會使用這些函數將伺服器安裝在主機電腦上。</span><span class="sxs-lookup"><span data-stu-id="a34a0-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a34a0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a34a0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a34a0-115">註冊 COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="a34a0-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 