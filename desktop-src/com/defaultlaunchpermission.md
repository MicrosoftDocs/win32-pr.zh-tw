---
title: DefaultLaunchPermission
description: 定義存取控制清單 (ACL) 可啟動的類別，這些類別無法透過 LaunchPermission 登錄值指定自己的 ACL。
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- DefaultLaunchPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966829"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="10b1f-104">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="10b1f-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="10b1f-105">定義存取控制清單 (ACL) 可啟動的類別，這些類別無法透過 [**LaunchPermission**](launchpermission.md) 登錄值指定自己的 ACL。</span><span class="sxs-lookup"><span data-stu-id="10b1f-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="10b1f-106">不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="10b1f-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="10b1f-107">如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="10b1f-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="10b1f-108">如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="10b1f-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="10b1f-109">登錄項目</span><span class="sxs-lookup"><span data-stu-id="10b1f-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="10b1f-110">備註</span><span class="sxs-lookup"><span data-stu-id="10b1f-110">Remarks</span></span>

<span data-ttu-id="10b1f-111">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="10b1f-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="10b1f-112">預設存取權限如下所示：</span><span class="sxs-lookup"><span data-stu-id="10b1f-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="10b1f-113">系統管理員：允許啟動</span><span class="sxs-lookup"><span data-stu-id="10b1f-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="10b1f-114">系統：允許啟動</span><span class="sxs-lookup"><span data-stu-id="10b1f-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="10b1f-115">互動式：允許啟動</span><span class="sxs-lookup"><span data-stu-id="10b1f-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="10b1f-116">如果為伺服器設定 [**LaunchPermission**](launchpermission.md) 值，其優先順序會高於 **DefaultLaunchPermission** 值。</span><span class="sxs-lookup"><span data-stu-id="10b1f-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="10b1f-117">當您收到本機或遠端要求以啟動伺服器，其 [**AppID**](appid-key.md) 金鑰本身沒有 **LaunchPermission** 值時，會在模擬用戶端時檢查此值所描述的 ACL，而其成功允許或不允許啟動類別程式碼。</span><span class="sxs-lookup"><span data-stu-id="10b1f-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="10b1f-118">此值提供簡單的集中式系統管理層級，讓您在電腦上以其他方式 unadministered 類別來啟動存取。</span><span class="sxs-lookup"><span data-stu-id="10b1f-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="10b1f-119">例如，系統管理員可能會使用 DCOMCNFG 工具來設定系統，以允許 Power Users 的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="10b1f-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="10b1f-120">因此，OLE 會限制對 Power Users 群組的成員啟動類別程式碼的要求。</span><span class="sxs-lookup"><span data-stu-id="10b1f-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="10b1f-121">系統管理員接著可以設定個別類別的啟動許可權，以將啟動類別程式碼的能力授與其他群組或個別使用者（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="10b1f-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10b1f-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="10b1f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b1f-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="10b1f-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="10b1f-124">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="10b1f-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="10b1f-125">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="10b1f-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




