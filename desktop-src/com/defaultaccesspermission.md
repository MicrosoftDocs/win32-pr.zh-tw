---
title: DefaultAccessPermission
description: 設定存取控制清單 (ACL) 可存取沒有 AccessPermission 設定之類別的主體。
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- DefaultAccessPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969836"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="b39d1-104">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="b39d1-104">DefaultAccessPermission</span></span>

<span data-ttu-id="b39d1-105">設定存取控制清單 (ACL) 可存取沒有 [**AccessPermission**](accesspermission.md) 設定之類別的主體。</span><span class="sxs-lookup"><span data-stu-id="b39d1-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="b39d1-106">此 ACL 僅供未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式使用，而且在其 [**AppID**](appid-key.md)金鑰底下沒有 **AccessPermission** 值。</span><span class="sxs-lookup"><span data-stu-id="b39d1-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="b39d1-107">不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b39d1-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="b39d1-108">如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="b39d1-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="b39d1-109">如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="b39d1-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="b39d1-110">登錄項目</span><span class="sxs-lookup"><span data-stu-id="b39d1-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="b39d1-111">備註</span><span class="sxs-lookup"><span data-stu-id="b39d1-111">Remarks</span></span>

<span data-ttu-id="b39d1-112">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="b39d1-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="b39d1-113">伺服器中的 COM 執行時間會在模擬嘗試連接至物件的呼叫端時，檢查此值所描述的 ACL，而且其 success 會判斷是否允許或不允許存取。</span><span class="sxs-lookup"><span data-stu-id="b39d1-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="b39d1-114">如果存取檢查失敗，則不允許與物件的連接。</span><span class="sxs-lookup"><span data-stu-id="b39d1-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="b39d1-115">如果這個命名值不存在，則只允許伺服器主體和本機系統呼叫伺服器。</span><span class="sxs-lookup"><span data-stu-id="b39d1-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="b39d1-116">依預設，此值沒有任何專案。</span><span class="sxs-lookup"><span data-stu-id="b39d1-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="b39d1-117">只有伺服器主體和系統允許呼叫伺服器。</span><span class="sxs-lookup"><span data-stu-id="b39d1-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="b39d1-118">此值提供簡單的集中式系統管理，讓您能夠在電腦上執行物件的預設連接存取。</span><span class="sxs-lookup"><span data-stu-id="b39d1-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b39d1-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b39d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b39d1-120">**AccessPermission**</span><span class="sxs-lookup"><span data-stu-id="b39d1-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="b39d1-121">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="b39d1-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="b39d1-122">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="b39d1-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




