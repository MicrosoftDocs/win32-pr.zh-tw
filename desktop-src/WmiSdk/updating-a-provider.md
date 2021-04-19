---
description: 有時您可能需要在執行中的系統上安裝較新版本的提供者。
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: 更新提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997841"
---
# <a name="updating-a-provider"></a><span data-ttu-id="6d191-103">更新提供者</span><span class="sxs-lookup"><span data-stu-id="6d191-103">Updating a Provider</span></span>

<span data-ttu-id="6d191-104">有時您可能需要在執行中的系統上安裝較新版本的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="6d191-105">如果您的提供者是安裝成 DLL，您可以安裝新的提供者，而不需要重新開機服務、重新開機電腦，或在當時使用 WMI 影響任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="6d191-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="6d191-106">下列程式說明如何更新提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="6d191-107">**更新提供者**</span><span class="sxs-lookup"><span data-stu-id="6d191-107">**To update a provider**</span></span>

1.  <span data-ttu-id="6d191-108">建立新的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="6d191-109">使用不同的 DLL 名稱和不同的 **CLSID** 來編譯新的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="6d191-110">例如，將 Myprov.dll 變更為 Myprov1.dll，並將 **clsid \_ MyProProv** 變更為 **clsid \_ MyProv** 1。</span><span class="sxs-lookup"><span data-stu-id="6d191-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="6d191-111">修改提供者註冊 MOF 檔案，以使用新的 CLSID (CLSID \_ MyProv1) ，但 ( "MyProv" ) 相同的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="6d191-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="6d191-112">安裝新的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="6d191-113">將新的提供者 DLL 連同舊的名稱一起複製。</span><span class="sxs-lookup"><span data-stu-id="6d191-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="6d191-114">自行註冊新的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-114">Self-register the new provider.</span></span>

        <span data-ttu-id="6d191-115">例如，使用 **regsvr32** **myprov1.dll** 命令來註冊新的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="6d191-116">編譯新的提供者註冊 MOF，進而覆寫舊的提供者註冊。</span><span class="sxs-lookup"><span data-stu-id="6d191-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="6d191-117">到目前為止，舊的提供者完全正常運作;新的提供者現在已可完全運作。</span><span class="sxs-lookup"><span data-stu-id="6d191-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="6d191-118">如有必要，請移除舊版本的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="6d191-119">取消註冊舊的 DLL。</span><span class="sxs-lookup"><span data-stu-id="6d191-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="6d191-120">例如，使用 **regsvr32** **/umyprov.dll** 命令取消註冊舊的 DLL。</span><span class="sxs-lookup"><span data-stu-id="6d191-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="6d191-121">藉由呼叫 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa)，標記要在重新開機時刪除的舊 DLL。</span><span class="sxs-lookup"><span data-stu-id="6d191-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="6d191-122">您可以採取類似的步驟來升級本機伺服器執行的提供者。</span><span class="sxs-lookup"><span data-stu-id="6d191-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d191-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d191-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d191-124">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="6d191-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="6d191-125">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="6d191-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="6d191-126">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="6d191-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
