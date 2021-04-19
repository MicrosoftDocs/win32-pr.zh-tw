---
title: DO_DOWNLOAD_ENUM_CATEGORY 結構
description: 由 **IDOManager：： EnumDownloads** 用來依特定屬性的值篩選下載列舉。
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106966018"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="2d314-104">DO_DOWNLOAD_ENUM_CATEGORY 結構</span><span class="sxs-lookup"><span data-stu-id="2d314-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="2d314-105">**IDOManager：： EnumDownloads** 會使用 **DO_DOWNLOAD_ENUM_CATEGORY** 結構，根據特定屬性的值篩選下載列舉。</span><span class="sxs-lookup"><span data-stu-id="2d314-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d314-106">語法</span><span class="sxs-lookup"><span data-stu-id="2d314-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="2d314-107">成員</span><span class="sxs-lookup"><span data-stu-id="2d314-107">Members</span></span>

`Property`

<span data-ttu-id="2d314-108">要用於下載列舉的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="2d314-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="2d314-109">這些屬性支援列舉用途。</span><span class="sxs-lookup"><span data-stu-id="2d314-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="2d314-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="2d314-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="2d314-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="2d314-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="2d314-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="2d314-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="2d314-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="2d314-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="2d314-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="2d314-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="2d314-115">屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2d314-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d314-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d314-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2d314-117">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="2d314-117">**Minimum supported client**</span></span> | <span data-ttu-id="2d314-118">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d314-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2d314-119">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="2d314-119">**Minimum supported server**</span></span> | <span data-ttu-id="2d314-120">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d314-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2d314-121">**標頭**</span><span class="sxs-lookup"><span data-stu-id="2d314-121">**Header**</span></span> | <span data-ttu-id="2d314-122">Do。h</span><span class="sxs-lookup"><span data-stu-id="2d314-122">Do.h</span></span> |
