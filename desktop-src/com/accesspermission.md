---
title: AccessPermission
description: 描述可存取此類別實例之主體 (ACL) 的存取控制清單。 只有未呼叫 CoInitializeSecurity 的應用程式才會使用此 ACL。
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- AccessPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463737"
---
# <a name="accesspermission"></a><span data-ttu-id="62ea0-105">AccessPermission</span><span class="sxs-lookup"><span data-stu-id="62ea0-105">AccessPermission</span></span>

<span data-ttu-id="62ea0-106">描述可存取此類別實例之主體 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="62ea0-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="62ea0-107">只有未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式才會使用此 ACL。</span><span class="sxs-lookup"><span data-stu-id="62ea0-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="62ea0-108">登錄項目</span><span class="sxs-lookup"><span data-stu-id="62ea0-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="62ea0-109">備註</span><span class="sxs-lookup"><span data-stu-id="62ea0-109">Remarks</span></span>

<span data-ttu-id="62ea0-110">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="62ea0-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="62ea0-111">它包含描述存取控制清單 (ACL) 的資料，這些主體可存取此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="62ea0-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="62ea0-112">收到連接到這個類別之現有物件的要求時，會由在模擬呼叫端時呼叫的應用程式檢查 ACL。</span><span class="sxs-lookup"><span data-stu-id="62ea0-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="62ea0-113">如果存取檢查失敗，則不允許連接。</span><span class="sxs-lookup"><span data-stu-id="62ea0-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="62ea0-114">如果這個命名值不存在，就會測試 [**DefaultAccessPermission**](defaultaccesspermission.md) ACL，以判斷是否允許連接。</span><span class="sxs-lookup"><span data-stu-id="62ea0-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="62ea0-115">針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或未使用 [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) 介面來指定 AppID 的應用程式，應用程式二進位檔的可執行檔必須對應到應用程式的 appid （如 [**AppID**](appid.md)中所述）。</span><span class="sxs-lookup"><span data-stu-id="62ea0-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="62ea0-116">這是必要的，如此 COM 才能找出應用程式的 AppID。</span><span class="sxs-lookup"><span data-stu-id="62ea0-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62ea0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="62ea0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62ea0-118">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="62ea0-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="62ea0-119">**DefaultAccessPermission**</span><span class="sxs-lookup"><span data-stu-id="62ea0-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="62ea0-120">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="62ea0-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 