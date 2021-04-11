---
title: LaunchPermission
description: 描述可為此類別啟動新伺服器之主體 (ACL) 的存取控制清單。 此值可以在任何 AppID 金鑰下新增，以限制特定類別的遠端用戶端啟用。
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- LaunchPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022099"
---
# <a name="launchpermission"></a><span data-ttu-id="f7158-105">LaunchPermission</span><span class="sxs-lookup"><span data-stu-id="f7158-105">LaunchPermission</span></span>

<span data-ttu-id="f7158-106">描述可為此類別啟動新伺服器之主體 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="f7158-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="f7158-107">此值可以在任何 [**AppID**](appid-key.md) 金鑰下新增，以限制特定類別的遠端用戶端啟用。</span><span class="sxs-lookup"><span data-stu-id="f7158-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f7158-108">登錄項目</span><span class="sxs-lookup"><span data-stu-id="f7158-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="f7158-109">備註</span><span class="sxs-lookup"><span data-stu-id="f7158-109">Remarks</span></span>

<span data-ttu-id="f7158-110">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="f7158-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="f7158-111">在收到本機或遠端要求以啟動此類別的伺服器時，會在模擬用戶端時檢查此值所描述的 ACL，而且其成功允許或不允許啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7158-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="f7158-112">如果此值不存在，則會以相同的方式檢查 [**DefaultLaunchPermission**](defaultlaunchpermission.md) 值，以判斷是否可以啟動類別程式碼。</span><span class="sxs-lookup"><span data-stu-id="f7158-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7158-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7158-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7158-114">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="f7158-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="f7158-115">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="f7158-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="f7158-116">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="f7158-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




