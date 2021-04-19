---
description: 當受保護的存放區顯示使用者介面時，定義其提示行為。
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: 'PST_PROMPTINFO 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993345"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="6ff53-103">PST \_ PROMPTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="6ff53-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="6ff53-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6ff53-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6ff53-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="6ff53-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6ff53-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="6ff53-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6ff53-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="6ff53-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6ff53-108">當受保護的存放區顯示使用者介面時，定義其提示行為。</span><span class="sxs-lookup"><span data-stu-id="6ff53-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff53-109">語法</span><span class="sxs-lookup"><span data-stu-id="6ff53-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="6ff53-110">成員</span><span class="sxs-lookup"><span data-stu-id="6ff53-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ff53-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="6ff53-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="6ff53-112">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="6ff53-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ff53-113">**dwPromptFlags**</span><span class="sxs-lookup"><span data-stu-id="6ff53-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6ff53-114">會忽略此旗標。</span><span class="sxs-lookup"><span data-stu-id="6ff53-114">This flag is ignored.</span></span>



| <span data-ttu-id="6ff53-115">值</span><span class="sxs-lookup"><span data-stu-id="6ff53-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="6ff53-116">意義</span><span class="sxs-lookup"><span data-stu-id="6ff53-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="6ff53-117"><dt>**PST \_PF \_ 一律 \_ 顯示**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6ff53-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6ff53-118">要求提供者顯示提示對話方塊給使用者，即使此存取不需要。</span><span class="sxs-lookup"><span data-stu-id="6ff53-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="6ff53-119"><dt>**PST \_PF \_ 絕不會 \_ 顯示**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6ff53-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="6ff53-120">不要向使用者顯示提示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6ff53-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="6ff53-121">**hwndApp**</span><span class="sxs-lookup"><span data-stu-id="6ff53-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="6ff53-122">使用者介面的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ff53-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="6ff53-123">**HwndApp** 成員會決定使用者介面的出現位置。</span><span class="sxs-lookup"><span data-stu-id="6ff53-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="6ff53-124">如果傳遞 **Null** ，則會將桌面視為父視窗。</span><span class="sxs-lookup"><span data-stu-id="6ff53-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="6ff53-125">**szPrompt**</span><span class="sxs-lookup"><span data-stu-id="6ff53-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="6ff53-126">提示字串。</span><span class="sxs-lookup"><span data-stu-id="6ff53-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ff53-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ff53-127">Requirements</span></span>



| <span data-ttu-id="6ff53-128">需求</span><span class="sxs-lookup"><span data-stu-id="6ff53-128">Requirement</span></span> | <span data-ttu-id="6ff53-129">值</span><span class="sxs-lookup"><span data-stu-id="6ff53-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff53-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6ff53-130">Header</span></span><br/> | <dl> <span data-ttu-id="6ff53-131"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff53-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff53-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ff53-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff53-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="6ff53-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="6ff53-134">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="6ff53-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="6ff53-135">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="6ff53-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="6ff53-136">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="6ff53-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
