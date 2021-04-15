---
description: 包含檔管理員用來加入功能表或工具列命令專案之說明字串的資訊。
title: 'FMS_HELPSTRING 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991594"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="aca66-103">FMS \_ HELPSTRING 結構</span><span class="sxs-lookup"><span data-stu-id="aca66-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="aca66-104">包含檔管理員用來加入功能表或工具列命令專案之說明字串的資訊。</span><span class="sxs-lookup"><span data-stu-id="aca66-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca66-105">語法</span><span class="sxs-lookup"><span data-stu-id="aca66-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="aca66-106">成員</span><span class="sxs-lookup"><span data-stu-id="aca66-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aca66-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="aca66-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="aca66-108">類型： **INT**</span><span class="sxs-lookup"><span data-stu-id="aca66-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="aca66-109">命令專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aca66-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="aca66-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="aca66-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="aca66-111">類型： **HMENU**</span><span class="sxs-lookup"><span data-stu-id="aca66-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="aca66-112">功能表列的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aca66-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="aca66-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="aca66-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="aca66-114">類型： **\_ \_ wchar \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="aca66-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="aca66-115">以 null 終止的字串，此字串會接收解說文字。</span><span class="sxs-lookup"><span data-stu-id="aca66-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aca66-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="aca66-116">Requirements</span></span>



| <span data-ttu-id="aca66-117">需求</span><span class="sxs-lookup"><span data-stu-id="aca66-117">Requirement</span></span> | <span data-ttu-id="aca66-118">值</span><span class="sxs-lookup"><span data-stu-id="aca66-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aca66-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aca66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aca66-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aca66-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="aca66-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aca66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aca66-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aca66-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aca66-123">標頭</span><span class="sxs-lookup"><span data-stu-id="aca66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca66-124"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="aca66-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca66-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aca66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca66-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="aca66-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="aca66-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="aca66-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




