---
description: 在 [active 檔案管理員] 視窗中， ([目錄] 視窗或 [搜尋結果] 視窗) ，包含所選取檔案的相關資訊。
title: 'FMS_GETFILESEL 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842219"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="05ca5-103">FMS \_ GETFILESEL 結構</span><span class="sxs-lookup"><span data-stu-id="05ca5-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="05ca5-104">在 [active 檔案管理員] 視窗中， ([目錄] 視窗或 [搜尋結果] 視窗) ，包含所選取檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05ca5-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="05ca5-105">語法</span><span class="sxs-lookup"><span data-stu-id="05ca5-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="05ca5-106">成員</span><span class="sxs-lookup"><span data-stu-id="05ca5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="05ca5-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="05ca5-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="05ca5-108">類型： **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="05ca5-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="05ca5-109">建立檔案的時間和日期。</span><span class="sxs-lookup"><span data-stu-id="05ca5-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="05ca5-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="05ca5-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="05ca5-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="05ca5-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="05ca5-112">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="05ca5-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="05ca5-113">**bAttr**</span><span class="sxs-lookup"><span data-stu-id="05ca5-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="05ca5-114">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="05ca5-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="05ca5-115">檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="05ca5-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="05ca5-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="05ca5-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="05ca5-117">類型： **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="05ca5-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="05ca5-118">以 null 結束的完整路徑和所選取檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="05ca5-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05ca5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="05ca5-119">Requirements</span></span>



| <span data-ttu-id="05ca5-120">需求</span><span class="sxs-lookup"><span data-stu-id="05ca5-120">Requirement</span></span> | <span data-ttu-id="05ca5-121">值</span><span class="sxs-lookup"><span data-stu-id="05ca5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05ca5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05ca5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05ca5-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05ca5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="05ca5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05ca5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05ca5-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05ca5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05ca5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="05ca5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="05ca5-127"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="05ca5-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ca5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05ca5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ca5-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="05ca5-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




