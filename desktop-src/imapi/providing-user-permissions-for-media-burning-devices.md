---
title: 提供媒體燒錄裝置的使用者權限
description: 根據預設，Windows Vista 和 Windows Server 2008 都會將讀取/寫入權限授與直接登入電腦的系統管理員和使用者)  (中繼使用者。
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104195663"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="ee769-103">提供媒體燒錄裝置的使用者權限</span><span class="sxs-lookup"><span data-stu-id="ee769-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="ee769-104">根據預設，Windows Vista 和 Windows Server 2008 都會將讀取/寫入權限授與直接登入電腦的系統管理員和使用者)  (中繼使用者。</span><span class="sxs-lookup"><span data-stu-id="ee769-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="ee769-105">不過，在 Windows XP 與 Windows Server 2003 中，系統管理員必須將這些裝置的讀取/寫入權限授與其他使用者群組。</span><span class="sxs-lookup"><span data-stu-id="ee769-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="ee769-106">系統管理員可以為 power 使用者和互動式使用者調整特定裝置的相關許可權。</span><span class="sxs-lookup"><span data-stu-id="ee769-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="ee769-107">若要在 Windows XP 中到達適當的群組許可權面板，請按一下 [ **開始**]，再按一下 [ **執行**]，輸入 **Gpedit.msc**，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="ee769-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="ee769-108">在群組原則介面中，依序展開 [ **電腦** 設定]、[ **Windows 設定**]、[ **安全性設定**]、[ **本機原則**]，然後按兩下 [ **安全性選項**]。</span><span class="sxs-lookup"><span data-stu-id="ee769-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![顯示 [群組原則] 視窗的螢幕擷取畫面，其中已從 [原則] 窗格中選取原則。](images/gpolpanel.jpg)

<span data-ttu-id="ee769-110">在此面板中，系統管理員必須指定兩個裝置選項的設定，以提供必要的群組許可權：</span><span class="sxs-lookup"><span data-stu-id="ee769-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="ee769-111">將「裝置：限制僅限本機登入使用者的 CD-ROM 存取」設為 **啟用**</span><span class="sxs-lookup"><span data-stu-id="ee769-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="ee769-112">將「裝置：允許格式化及退出卸載式媒體」設定給系統 **管理員和 Power Users**。</span><span class="sxs-lookup"><span data-stu-id="ee769-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="ee769-113">您也可以將此選項設定為 [系統管理員] 和 [ **互動式使用者**]，以模擬 Windows Vista 許可權。</span><span class="sxs-lookup"><span data-stu-id="ee769-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="ee769-114">雖然 Windows XP 或 Windows Server 2003 中沒有特定的 UI 可供使用 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 或 [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)，但您可以使用這些 api 來授與自訂使用者群組裝置許可權。</span><span class="sxs-lookup"><span data-stu-id="ee769-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="ee769-115">例如，對 **SetSecurityInfo** 的呼叫會將許可權授與使用者群組。</span><span class="sxs-lookup"><span data-stu-id="ee769-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="ee769-116">此 API 的許可權變更是暫時性的，不會在重新開機時持續保存。</span><span class="sxs-lookup"><span data-stu-id="ee769-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="ee769-117">不過，呼叫 [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) 將會執行登錄中的許可權變更，而這些變更會在重新開機時保存。</span><span class="sxs-lookup"><span data-stu-id="ee769-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee769-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee769-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee769-119">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="ee769-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="ee769-120">**SetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="ee769-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="ee769-121">SetupDiSetDeviceRegistryProperty</span><span class="sxs-lookup"><span data-stu-id="ee769-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 