---
description: Windows 密碼篩選 DLL （Passfilt.dll）會在本機系統帳戶的安全性內容中執行，並協助您篩選網域或本機帳戶密碼。
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: 安裝和註冊密碼篩選 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849454"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="71915-103">安裝和註冊密碼篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="71915-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="71915-104">您可以使用 Windows 密碼篩選器來篩選網域或本機帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="71915-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="71915-105">若要使用網域帳戶的密碼篩選，請在網域中的每個網域控制站上安裝並註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="71915-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="71915-106">請執行下列步驟來安裝您的密碼篩選。</span><span class="sxs-lookup"><span data-stu-id="71915-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="71915-107">您可以手動執行這些步驟，也可以撰寫安裝程式來執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="71915-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="71915-108">您必須是系統管理員或屬於系統管理員群組，才能執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="71915-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="71915-109">**安裝和註冊 Windows 密碼篩選 DLL**</span><span class="sxs-lookup"><span data-stu-id="71915-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="71915-110">將 DLL 複製到網域控制站或本機電腦上的 Windows 安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="71915-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="71915-111">在標準安裝中，預設資料夾為 \\ Windows \\ System32。</span><span class="sxs-lookup"><span data-stu-id="71915-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="71915-112">請確定您為32位電腦建立32位密碼篩選 DLL，並為64位電腦建立64位密碼篩選 DLL，然後將它們複製到適當的位置。</span><span class="sxs-lookup"><span data-stu-id="71915-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="71915-113">若要註冊密碼篩選器，請更新下列系統登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="71915-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="71915-114">如果 **通知封裝** 子機碼存在，請將您的 DLL 名稱新增至現有的值資料。</span><span class="sxs-lookup"><span data-stu-id="71915-114">If the **Notification Packages** subkey exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="71915-115">請勿覆寫現有的值，而且不包含 .dll 副檔名。</span><span class="sxs-lookup"><span data-stu-id="71915-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="71915-116">如果 **通知封裝** 子機碼不存在，請新增它，然後為值資料指定 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="71915-116">If the **Notification Packages** subkey does not exist, add it, and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="71915-117">請勿包含 .dll 副檔名。</span><span class="sxs-lookup"><span data-stu-id="71915-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="71915-118">**通知套件** 子機碼可以加入多個套件。</span><span class="sxs-lookup"><span data-stu-id="71915-118">The **Notification Packages** subkey can add multiple packages.</span></span>

3.  <span data-ttu-id="71915-119">尋找 [密碼複雜性] 設定。</span><span class="sxs-lookup"><span data-stu-id="71915-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="71915-120">在主控台中，依序按一下 [ **效能及維護**]、[系統 **管理工具**]、[ **本機安全性原則**]、[ **帳戶原則**]，然後按兩下 [ **密碼原則**]。</span><span class="sxs-lookup"><span data-stu-id="71915-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="71915-121">若要強制執行預設的 Windows 密碼篩選器和自訂密碼篩選器，請確定已啟用 [ **密碼必須符合複雜性需求** ] 原則設定。</span><span class="sxs-lookup"><span data-stu-id="71915-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="71915-122">否則，請停用 [ **密碼必須符合複雜性需求** ] 原則設定。</span><span class="sxs-lookup"><span data-stu-id="71915-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71915-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="71915-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71915-124">密碼篩選程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="71915-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="71915-125">強式密碼強制執行和 Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="71915-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="71915-126">密碼篩選函數</span><span class="sxs-lookup"><span data-stu-id="71915-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



