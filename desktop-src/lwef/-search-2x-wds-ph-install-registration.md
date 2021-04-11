---
title: " (舊版 Windows 環境功能安裝和註冊通訊協定處理常式) "
description: 安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置並加以註冊。
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317083"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="7df57-103"> (舊版 Windows 環境功能安裝和註冊通訊協定處理常式) </span><span class="sxs-lookup"><span data-stu-id="7df57-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="7df57-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="7df57-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7df57-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="7df57-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="7df57-106">安裝 **通訊協定處理常式** 牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置並加以註冊。</span><span class="sxs-lookup"><span data-stu-id="7df57-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="7df57-107">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="7df57-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="7df57-108">安裝指導方針</span><span class="sxs-lookup"><span data-stu-id="7df57-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="7df57-109">註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="7df57-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="7df57-110">註冊 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="7df57-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="7df57-111">安裝指導方針</span><span class="sxs-lookup"><span data-stu-id="7df57-111">Installation Guidelines</span></span>

<span data-ttu-id="7df57-112">通訊協定處理常式應該執行自我註冊以進行安裝，並遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="7df57-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="7df57-113">安裝程式必須使用 EXE 或 MSI 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="7df57-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="7df57-114">必須提供版本資訊。</span><span class="sxs-lookup"><span data-stu-id="7df57-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="7df57-115">每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。</span><span class="sxs-lookup"><span data-stu-id="7df57-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="7df57-116">安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。</span><span class="sxs-lookup"><span data-stu-id="7df57-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="7df57-117">如果先前的增益集遭到覆寫，安裝程式應通知使用者。</span><span class="sxs-lookup"><span data-stu-id="7df57-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="7df57-118">如果較新的增益集覆寫了先前的增益集，就應該能夠還原先前增益集的功能，並使它成為該檔案類型的預設增益集。</span><span class="sxs-lookup"><span data-stu-id="7df57-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="7df57-119">註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="7df57-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="7df57-120">您必須在登錄中建立14個專案，以註冊通訊協定處理常式元件，其中：</span><span class="sxs-lookup"><span data-stu-id="7df57-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="7df57-121">*Ver \_Ind \_ ProgID* 是通訊協定處理常式執行的獨立 ProgID 版本</span><span class="sxs-lookup"><span data-stu-id="7df57-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="7df57-122">*Ver \_Dep \_ ProgID* 是通訊協定處理常式執行的相依 ProgID 版本</span><span class="sxs-lookup"><span data-stu-id="7df57-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="7df57-123">*Clsid \_ 1* 是通訊協定處理常式執行的 clsid</span><span class="sxs-lookup"><span data-stu-id="7df57-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="7df57-124">使用下列索引鍵和值註冊版本獨立 ProgID：</span><span class="sxs-lookup"><span data-stu-id="7df57-124">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="7df57-125">使用下列索引鍵和值註冊版本相依 ProgID：</span><span class="sxs-lookup"><span data-stu-id="7df57-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="7df57-126">使用下列索引鍵和值註冊通訊協定處理常式的 CLSID：</span><span class="sxs-lookup"><span data-stu-id="7df57-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  <span data-ttu-id="7df57-127">使用 Windows Desktop Search 註冊通訊協定處理常式：</span><span class="sxs-lookup"><span data-stu-id="7df57-127">Register the protocol handler with Windows Desktop Search:</span></span>

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a><span data-ttu-id="7df57-128">註冊 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="7df57-128">To Register Shell Extensions</span></span>

<span data-ttu-id="7df57-129">您必須在登錄中建立兩個專案，才能註冊通訊協定處理常式的 Shell 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="7df57-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




