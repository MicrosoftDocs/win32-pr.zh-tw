---
description: 描述類型或子類型。
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: 'PST_TYPEINFO 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995037"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="66746-103">PST \_ TYPEINFO 結構</span><span class="sxs-lookup"><span data-stu-id="66746-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="66746-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="66746-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="66746-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="66746-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="66746-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="66746-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="66746-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="66746-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="66746-108">描述類型或子類型。</span><span class="sxs-lookup"><span data-stu-id="66746-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="66746-109">語法</span><span class="sxs-lookup"><span data-stu-id="66746-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="66746-110">成員</span><span class="sxs-lookup"><span data-stu-id="66746-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="66746-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="66746-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="66746-112">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="66746-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="66746-113">**szDisplayName**</span><span class="sxs-lookup"><span data-stu-id="66746-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="66746-114">代表型別之顯示名稱的寬字元字串指標。</span><span class="sxs-lookup"><span data-stu-id="66746-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66746-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="66746-115">Requirements</span></span>



| <span data-ttu-id="66746-116">需求</span><span class="sxs-lookup"><span data-stu-id="66746-116">Requirement</span></span> | <span data-ttu-id="66746-117">值</span><span class="sxs-lookup"><span data-stu-id="66746-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66746-118">標頭</span><span class="sxs-lookup"><span data-stu-id="66746-118">Header</span></span><br/> | <dl> <span data-ttu-id="66746-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="66746-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66746-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66746-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66746-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="66746-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="66746-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="66746-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="66746-123">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="66746-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="66746-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="66746-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
