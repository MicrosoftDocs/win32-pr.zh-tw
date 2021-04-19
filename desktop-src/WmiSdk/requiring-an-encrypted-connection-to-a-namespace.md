---
description: 您可以要求用戶端腳本和應用程式建立加密連接以進行驗證，方法是將 RequiresEncryption 限定詞新增至建立命名空間的受控物件格式 (MOF) mof 檔案。
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: 需要命名空間的加密連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996982"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="e6661-103">需要命名空間的加密連接</span><span class="sxs-lookup"><span data-stu-id="e6661-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="e6661-104">您可以要求用戶端腳本和應用程式建立加密連接以進行驗證，方法是將 **RequiresEncryption** 限定詞新增至建立命名空間的受控物件格式 (mof) mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="e6661-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="e6661-105">對 WMI 命名空間進行加密的連線，會在腳本) 中指定 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權** (或 **PktPrivacy** 以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e6661-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="e6661-106">**RequiresEncryption** 限定詞會讓 WMI 拒絕任何傳入的資料要求，除非它們明確地使用加密的驗證。</span><span class="sxs-lookup"><span data-stu-id="e6661-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="e6661-107">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性等級](setting-the-default-process-security-level-using-vbscript.md) 或 [使用 c + + 設定驗證](setting-authentication-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="e6661-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="e6661-108">您也可以藉由新增這個屬性來修改現有的命名空間，然後再次編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="e6661-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="e6661-109">**RequiresEncryption** 可用於具有 [pragma 命名空間](pragma-namespace.md)預處理器指令的 [*MOF*](gloss-m.md)中。</span><span class="sxs-lookup"><span data-stu-id="e6661-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="e6661-110">下列程式會將命名空間設定為需要加密的連接。</span><span class="sxs-lookup"><span data-stu-id="e6661-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="e6661-111">**設定必要的加密**</span><span class="sxs-lookup"><span data-stu-id="e6661-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="e6661-112">建立受控物件格式 (MOF) 檔，或修改現有的 MOF 檔案來定義命名空間。</span><span class="sxs-lookup"><span data-stu-id="e6661-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="e6661-113">下列程式碼範例會示範要修改的命名空間是 *根 \\ MyNamespace* ，而檔案名為 *MyNamespace \_ security. mof*。</span><span class="sxs-lookup"><span data-stu-id="e6661-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="e6661-114">**RequiresEncryption** 具有布林資料類型，因此必須設定為 **True** 或 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6661-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="e6661-115">執行 [**mofcomp.exe**](mofcomp.md) 以編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="e6661-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="e6661-116">**c： \\ Mofcomp.exe MyNamespace \_ security. mof**</span><span class="sxs-lookup"><span data-stu-id="e6661-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="e6661-117">在 c + + 中，請使用 [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 方法。</span><span class="sxs-lookup"><span data-stu-id="e6661-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="e6661-118">WMI 會拒絕使用預設驗證層級的用戶端，因為 DCOM 會將安全性協調為執行 WMI 服務的 SVCHOST 進程所需的層級。</span><span class="sxs-lookup"><span data-stu-id="e6661-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="e6661-119">如需服務主機的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="e6661-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="e6661-120">如需有關連接到 WMI 命名空間時設定驗證層級的詳細資訊，請參閱使用 [c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md)、使用 [c + + 設定驗證](setting-authentication-using-c-.md)，或 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="e6661-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="e6661-121">在非同步回呼連接上傳回資料時，WMI 會將拒絕存取的訊息傳回給提出要求的電腦。</span><span class="sxs-lookup"><span data-stu-id="e6661-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="e6661-122">WMI 也會使用加密的命名空間，在電腦的 NT 事件記錄檔中建立記錄專案，表示無法建立用戶端的安全連線。</span><span class="sxs-lookup"><span data-stu-id="e6661-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="e6661-123">從 Windows Vista 開始，WbemCore 檔案已不再存在。</span><span class="sxs-lookup"><span data-stu-id="e6661-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="e6661-124">您可以檢查 NT 事件記錄檔中的專案，指出已拒絕需要加密的命名空間的輸入資料要求。</span><span class="sxs-lookup"><span data-stu-id="e6661-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6661-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6661-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6661-126">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="e6661-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="e6661-127">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="e6661-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="e6661-128">保護遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="e6661-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



