---
title: DoNotAddAllApplicationPackagesToRestrictions
description: 判斷依預設，RPCSS 是否會自動 \_ 將所有應用程式 \_ 封裝 SID 附加至 COM 限制。
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371916"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a><span data-ttu-id="6965c-103">DoNotAddAllApplicationPackagesToRestrictions</span><span class="sxs-lookup"><span data-stu-id="6965c-103">DoNotAddAllApplicationPackagesToRestrictions</span></span>

<span data-ttu-id="6965c-104">判斷依預設，RPCSS 是否會自動 \_ 將所有應用程式 \_ 封裝 SID 附加至 COM 限制。</span><span class="sxs-lookup"><span data-stu-id="6965c-104">Determines whether RPCSS automatically appends an ALL\_APPLICATION\_PACKAGES SID to COM restrictions by default.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6965c-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="6965c-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a><span data-ttu-id="6965c-106">備註</span><span class="sxs-lookup"><span data-stu-id="6965c-106">Remarks</span></span>

<span data-ttu-id="6965c-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="6965c-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="6965c-108">值</span><span class="sxs-lookup"><span data-stu-id="6965c-108">Value</span></span> | <span data-ttu-id="6965c-109">描述</span><span class="sxs-lookup"><span data-stu-id="6965c-109">Description</span></span>                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6965c-110">0</span><span class="sxs-lookup"><span data-stu-id="6965c-110">0</span></span>     | <span data-ttu-id="6965c-111">從 Windows 7 遷移至 Windows 8 時停用 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6965c-111">Disables Windows Store apps upon migration from Windows 7 to Windows 8.</span></span>                   |
| <span data-ttu-id="6965c-112">1</span><span class="sxs-lookup"><span data-stu-id="6965c-112">1</span></span>     | <span data-ttu-id="6965c-113">不會將所有 \_ 應用程式 \_ 封裝 SID 新增至 COM 限制。</span><span class="sxs-lookup"><span data-stu-id="6965c-113">Does not add the ALL\_APPLICATION\_PACKAGES SID to COM restrictions.</span></span> <span data-ttu-id="6965c-114">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="6965c-114">This is the default.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6965c-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="6965c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6965c-116">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="6965c-116">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




