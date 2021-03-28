---
description: 允許回呼物件提供網際網路區域資訊。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: 'SFVM_GETZONE 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514116"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="ecf40-104">SFVM \_ GETZONE 訊息</span><span class="sxs-lookup"><span data-stu-id="ecf40-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="ecf40-105">\[這項通知是透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 支援。</span><span class="sxs-lookup"><span data-stu-id="ecf40-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="ecf40-106">後續版本的 Windows 可能不支援此功能。\]</span><span class="sxs-lookup"><span data-stu-id="ecf40-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ecf40-107">允許回呼物件提供網際網路區域資訊。</span><span class="sxs-lookup"><span data-stu-id="ecf40-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="ecf40-108">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="ecf40-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="ecf40-109">參數</span><span class="sxs-lookup"><span data-stu-id="ecf40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf40-110">*區域* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ecf40-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf40-111">下列其中一個指出網際網路區域的值。</span><span class="sxs-lookup"><span data-stu-id="ecf40-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="ecf40-112">這些值會構成 [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) 列舉，定義于 urlmon.dll 中。</span><span class="sxs-lookup"><span data-stu-id="ecf40-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="ecf40-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="ecf40-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="ecf40-114">使用者的本機電腦上已有內容使用的區域。</span><span class="sxs-lookup"><span data-stu-id="ecf40-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="ecf40-115">使用者介面不會公開此區域。</span><span class="sxs-lookup"><span data-stu-id="ecf40-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="ecf40-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE \_ 內部網路**</span><span class="sxs-lookup"><span data-stu-id="ecf40-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="ecf40-117">用於內部網路上找到的內容的區域。</span><span class="sxs-lookup"><span data-stu-id="ecf40-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="ecf40-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ 信任**</span><span class="sxs-lookup"><span data-stu-id="ecf40-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="ecf40-119">用於網際網路上受信任網站的區域。</span><span class="sxs-lookup"><span data-stu-id="ecf40-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="ecf40-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE \_ 網際網路**</span><span class="sxs-lookup"><span data-stu-id="ecf40-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="ecf40-121">網際網路上大部分內容所使用的區域。</span><span class="sxs-lookup"><span data-stu-id="ecf40-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="ecf40-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE \_ 不受信任**</span><span class="sxs-lookup"><span data-stu-id="ecf40-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="ecf40-123">不受信任的網站所使用的區域。</span><span class="sxs-lookup"><span data-stu-id="ecf40-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecf40-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecf40-124">Requirements</span></span>



| <span data-ttu-id="ecf40-125">需求</span><span class="sxs-lookup"><span data-stu-id="ecf40-125">Requirement</span></span> | <span data-ttu-id="ecf40-126">值</span><span class="sxs-lookup"><span data-stu-id="ecf40-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf40-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecf40-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf40-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecf40-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ecf40-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecf40-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf40-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecf40-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ecf40-131">標頭</span><span class="sxs-lookup"><span data-stu-id="ecf40-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf40-132"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf40-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
