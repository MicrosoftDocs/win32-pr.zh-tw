---
description: 識別受保護儲存體資料的存取規則集。
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: 'PST_ACCESSRULESET 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995027"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="2b584-103">PST \_ ACCESSRULESET 結構</span><span class="sxs-lookup"><span data-stu-id="2b584-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="2b584-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2b584-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2b584-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="2b584-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2b584-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="2b584-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2b584-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="2b584-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2b584-108">識別受保護儲存體資料的存取規則集。</span><span class="sxs-lookup"><span data-stu-id="2b584-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b584-109">語法</span><span class="sxs-lookup"><span data-stu-id="2b584-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="2b584-110">成員</span><span class="sxs-lookup"><span data-stu-id="2b584-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b584-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="2b584-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="2b584-112">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="2b584-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="2b584-113">**cRules**</span><span class="sxs-lookup"><span data-stu-id="2b584-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="2b584-114">**RgRules** 陣列中的規則數目。</span><span class="sxs-lookup"><span data-stu-id="2b584-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="2b584-115">**rgRules**</span><span class="sxs-lookup"><span data-stu-id="2b584-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="2b584-116">[**PST \_ ACCESSRULE**](pst-accessrule.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="2b584-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b584-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b584-117">Requirements</span></span>



| <span data-ttu-id="2b584-118">需求</span><span class="sxs-lookup"><span data-stu-id="2b584-118">Requirement</span></span> | <span data-ttu-id="2b584-119">值</span><span class="sxs-lookup"><span data-stu-id="2b584-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b584-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2b584-120">Header</span></span><br/> | <dl> <span data-ttu-id="2b584-121"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b584-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b584-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b584-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b584-123">**PST \_ ACCESSRULE**</span><span class="sxs-lookup"><span data-stu-id="2b584-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="2b584-124">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="2b584-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
