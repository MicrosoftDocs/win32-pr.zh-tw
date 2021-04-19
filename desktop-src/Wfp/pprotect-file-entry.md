---
description: SfcGetFiles 函數所使用的結構。
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: 'PPROTECT_FILE_ENTRY 結構 (Sfcfiles .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000127"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="ce267-103">PPROTECT \_ 檔案 \_ 專案結構</span><span class="sxs-lookup"><span data-stu-id="ce267-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="ce267-104">\[此結構可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ce267-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ce267-105">此結構的支援已在 Windows Vista 和 Windows Server 2008 中移除。</span><span class="sxs-lookup"><span data-stu-id="ce267-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ce267-106">請改用 [WRP](wfp-functions.md) 函式中所列的支援函數。\]</span><span class="sxs-lookup"><span data-stu-id="ce267-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="ce267-107">[**SfcGetFiles**](sfcgetfiles.md)函數所使用的結構。</span><span class="sxs-lookup"><span data-stu-id="ce267-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce267-108">語法</span><span class="sxs-lookup"><span data-stu-id="ce267-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="ce267-109">成員</span><span class="sxs-lookup"><span data-stu-id="ce267-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce267-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="ce267-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="ce267-111">字串值的指標，其中包含原始程式檔的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ce267-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="ce267-112">如果未在安裝時重新命名檔案，則這會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ce267-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="ce267-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ce267-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="ce267-114">字串值的指標，其中包含目的地檔案名以及檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ce267-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="ce267-115">**InfName**</span><span class="sxs-lookup"><span data-stu-id="ce267-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="ce267-116">字串值的指標，其中包含提供版面配置資訊的 INF 檔案名。</span><span class="sxs-lookup"><span data-stu-id="ce267-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="ce267-117">使用預設版面配置時，此參數可能是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ce267-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce267-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce267-118">Requirements</span></span>



| <span data-ttu-id="ce267-119">需求</span><span class="sxs-lookup"><span data-stu-id="ce267-119">Requirement</span></span> | <span data-ttu-id="ce267-120">值</span><span class="sxs-lookup"><span data-stu-id="ce267-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce267-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce267-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce267-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce267-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce267-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce267-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce267-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce267-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce267-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ce267-125">End of client support</span></span><br/>    | <span data-ttu-id="ce267-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce267-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="ce267-127">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ce267-127">End of server support</span></span><br/>    | <span data-ttu-id="ce267-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce267-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="ce267-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ce267-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce267-130"><dt>Sfcfiles。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce267-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce267-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce267-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce267-132">**SfcGetFiles**</span><span class="sxs-lookup"><span data-stu-id="ce267-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




