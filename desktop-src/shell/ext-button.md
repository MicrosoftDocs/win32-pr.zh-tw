---
description: 包含有關檔案管理員延伸模組 DLL 新增至 [檔案管理員] 工具列之按鈕的資訊。
title: 'EXT_BUTTON 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843149"
---
# <a name="ext_button-structure"></a><span data-ttu-id="14df9-103">EXT \_ 按鈕結構</span><span class="sxs-lookup"><span data-stu-id="14df9-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="14df9-104">包含有關檔案管理員延伸模組 DLL 新增至 [檔案管理員] 工具列之按鈕的資訊。</span><span class="sxs-lookup"><span data-stu-id="14df9-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="14df9-105">語法</span><span class="sxs-lookup"><span data-stu-id="14df9-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="14df9-106">成員</span><span class="sxs-lookup"><span data-stu-id="14df9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="14df9-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="14df9-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="14df9-108">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="14df9-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="14df9-109">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="14df9-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="14df9-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="14df9-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="14df9-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="14df9-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="14df9-112">按鈕的說明字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="14df9-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="14df9-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="14df9-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="14df9-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="14df9-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="14df9-115">按鈕的樣式。</span><span class="sxs-lookup"><span data-stu-id="14df9-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14df9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="14df9-116">Requirements</span></span>



| <span data-ttu-id="14df9-117">需求</span><span class="sxs-lookup"><span data-stu-id="14df9-117">Requirement</span></span> | <span data-ttu-id="14df9-118">值</span><span class="sxs-lookup"><span data-stu-id="14df9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14df9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14df9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="14df9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14df9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="14df9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14df9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="14df9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14df9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14df9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="14df9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="14df9-124"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="14df9-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14df9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14df9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14df9-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="14df9-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="14df9-127">**FMS \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="14df9-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




