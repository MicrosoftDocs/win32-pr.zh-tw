---
description: 包含檔管理員用來新增由檔管理程式延伸模組 DLL 提供之自訂功能表的資訊。 此結構也提供差異值，可供延伸模組 DLL 在檔案管理員載入功能表之後，用來操作自訂功能表。
title: 'FMS_LOAD 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842189"
---
# <a name="fms_load-structure"></a><span data-ttu-id="43474-104">FMS \_ 載入結構</span><span class="sxs-lookup"><span data-stu-id="43474-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="43474-105">包含檔管理員用來新增由檔管理程式延伸模組 DLL 提供之自訂功能表的資訊。</span><span class="sxs-lookup"><span data-stu-id="43474-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="43474-106">此結構也提供差異值，可供延伸模組 DLL 在檔案管理員載入功能表之後，用來操作自訂功能表。</span><span class="sxs-lookup"><span data-stu-id="43474-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="43474-107">語法</span><span class="sxs-lookup"><span data-stu-id="43474-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="43474-108">成員</span><span class="sxs-lookup"><span data-stu-id="43474-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="43474-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="43474-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="43474-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="43474-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="43474-111">結構的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="43474-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="43474-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="43474-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="43474-113">類型： **TCHAR \[ 功能表 \_ 文字 \_ LEN \]**</span><span class="sxs-lookup"><span data-stu-id="43474-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="43474-114">在 [檔案管理員] 中出現在功能表列上的功能表項目之以 null 結束的名稱。</span><span class="sxs-lookup"><span data-stu-id="43474-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="43474-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="43474-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="43474-116">類型： **HMENU**</span><span class="sxs-lookup"><span data-stu-id="43474-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="43474-117">已新增至 [檔案管理員] 功能表列之快顯功能表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43474-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="43474-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="43474-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="43474-119">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="43474-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="43474-120">功能表項目差異值。</span><span class="sxs-lookup"><span data-stu-id="43474-120">The menu item delta value.</span></span> <span data-ttu-id="43474-121">為了避免與本身的功能表項目發生衝突，檔管理員會將此差異值新增至每個識別碼，以將 **hMenu** 成員所識別之快顯功能表中的功能表項目識別碼進行比對。</span><span class="sxs-lookup"><span data-stu-id="43474-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="43474-122">必須修改功能表項目的延伸模組 DLL 必須將 delta 值新增至功能表項目的識別碼，以識別專案。</span><span class="sxs-lookup"><span data-stu-id="43474-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="43474-123">此成員的值可能會因會話而異。</span><span class="sxs-lookup"><span data-stu-id="43474-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43474-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="43474-124">Requirements</span></span>



| <span data-ttu-id="43474-125">需求</span><span class="sxs-lookup"><span data-stu-id="43474-125">Requirement</span></span> | <span data-ttu-id="43474-126">值</span><span class="sxs-lookup"><span data-stu-id="43474-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43474-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43474-127">Minimum supported client</span></span><br/> | <span data-ttu-id="43474-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43474-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="43474-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43474-129">Minimum supported server</span></span><br/> | <span data-ttu-id="43474-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43474-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43474-131">標頭</span><span class="sxs-lookup"><span data-stu-id="43474-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="43474-132"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="43474-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43474-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43474-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43474-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="43474-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




