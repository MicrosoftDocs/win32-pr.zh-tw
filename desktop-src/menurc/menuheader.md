---
title: MENUHEADER 結構
description: 包含功能表資源的版本資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- MENUHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965694"
---
# <a name="menuheader-structure"></a><span data-ttu-id="85427-105">MENUHEADER 結構</span><span class="sxs-lookup"><span data-stu-id="85427-105">MENUHEADER structure</span></span>

<span data-ttu-id="85427-106">包含功能表資源的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="85427-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="85427-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="85427-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85427-108">語法</span><span class="sxs-lookup"><span data-stu-id="85427-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="85427-109">成員</span><span class="sxs-lookup"><span data-stu-id="85427-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="85427-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="85427-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="85427-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="85427-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="85427-112">功能表範本的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="85427-112">The version number of the menu template.</span></span> <span data-ttu-id="85427-113">此成員必須等於零，表示這是使用標準功能表範本建立的 [**RT \_ 功能表**](/windows/desktop/menurc/resource-types) 。</span><span class="sxs-lookup"><span data-stu-id="85427-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="85427-114">**cbHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="85427-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="85427-115">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="85427-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="85427-116">功能表範本標頭的大小。</span><span class="sxs-lookup"><span data-stu-id="85427-116">The size of the menu template header.</span></span> <span data-ttu-id="85427-117">如果您使用標準功能表範本建立的功能表，此值為零。</span><span class="sxs-lookup"><span data-stu-id="85427-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85427-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="85427-118">Requirements</span></span>



| <span data-ttu-id="85427-119">需求</span><span class="sxs-lookup"><span data-stu-id="85427-119">Requirement</span></span> | <span data-ttu-id="85427-120">值</span><span class="sxs-lookup"><span data-stu-id="85427-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="85427-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85427-121">Minimum supported client</span></span><br/> | <span data-ttu-id="85427-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85427-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="85427-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85427-123">Minimum supported server</span></span><br/> | <span data-ttu-id="85427-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85427-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="85427-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85427-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="85427-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="85427-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="85427-127">**MENUEX \_ 範本 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="85427-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="85427-128">**MENUEX \_ 範本 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="85427-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="85427-129">**MENUITEMTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="85427-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="85427-130">**MENUITEMTEMPLATEHEADER**</span><span class="sxs-lookup"><span data-stu-id="85427-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="85427-131">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="85427-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="85427-132">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="85427-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="85427-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="85427-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="85427-134">資源</span><span class="sxs-lookup"><span data-stu-id="85427-134">Resources</span></span>](resources.md)
</dt> </dl>

 

