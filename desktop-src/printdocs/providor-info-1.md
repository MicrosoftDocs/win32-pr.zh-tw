---
description: PROVIDOR \_ INFO \_ 1 結構會識別列印提供者。
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: 'PROVIDOR_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319971"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="960da-103">PROVIDOR \_ INFO \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="960da-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="960da-104">**PROVIDOR \_ INFO \_ 1** 結構會識別列印提供者。</span><span class="sxs-lookup"><span data-stu-id="960da-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="960da-105">語法</span><span class="sxs-lookup"><span data-stu-id="960da-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="960da-106">成員</span><span class="sxs-lookup"><span data-stu-id="960da-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="960da-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="960da-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="960da-108">以 null 結束的字串指標，該字串是列印提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="960da-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="960da-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="960da-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="960da-110">以 null 結束的環境字串指標，指定環境：提供者動態連結程式庫 (DLL) 是設計用來執行。</span><span class="sxs-lookup"><span data-stu-id="960da-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="960da-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="960da-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="960da-112">以 null 結束的字串指標，該字串是 provider .dll 的名稱。</span><span class="sxs-lookup"><span data-stu-id="960da-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="960da-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="960da-113">Requirements</span></span>



| <span data-ttu-id="960da-114">需求</span><span class="sxs-lookup"><span data-stu-id="960da-114">Requirement</span></span> | <span data-ttu-id="960da-115">值</span><span class="sxs-lookup"><span data-stu-id="960da-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960da-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="960da-116">Minimum supported client</span></span><br/> | <span data-ttu-id="960da-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="960da-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="960da-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="960da-118">Minimum supported server</span></span><br/> | <span data-ttu-id="960da-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="960da-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="960da-120">標頭</span><span class="sxs-lookup"><span data-stu-id="960da-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="960da-121"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="960da-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="960da-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="960da-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="960da-123">**\_ PROVIDOR \_ Info \_ 1W** (Unicode) 和 **\_ PROVIDOR \_ info \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="960da-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="960da-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="960da-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960da-125">列印</span><span class="sxs-lookup"><span data-stu-id="960da-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="960da-126">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="960da-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="960da-127">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="960da-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




